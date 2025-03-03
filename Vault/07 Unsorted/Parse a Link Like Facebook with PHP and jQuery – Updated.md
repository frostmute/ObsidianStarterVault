So I wanted to build a link parser like the one on Facebook, but didn’t find one that suited me. So I built one. My code is based off the code found [here](http://www.99points.info/2010/07/facebook-like-extracting-url-data-with-jquery-ajax-php/), but I rewrote much of it to be cleaner and to return JSON rather than HTML.

[DEMO](https://www.redsunsoft.com/demo/link_parser/) [DOWNLOAD](https://www.redsunsoft.com/demo/link_parser/link_parser.zip)

****Code Change – Feb 2nd, 2011****  
  
Added some refinements to the cleaning mechanism and greatly speed up image parser.

> [!NOTE]
> ### HTML
> ```
> <script src="http://ajax.googleapis.com/ajax/libs/jquery/1.4.4/jquery.min.js"></script>
> <style>
>    #atc_bar{width:500px;}
>    #attach_content{border:1px solid #ccc;padding:10px;margin-top:10px;}
>    #atc_images {width:100px;height:120px;overflow:hidden;float:left;}
>    #atc_info {width:350px;float:left;height:100px;text-align:left; padding:10px;}
>    #atc_title {font-size:14px;display:block;}
>    #atc_url {font-size:10px;display:block;}
>    #atc_desc {font-size:12px;}
>    #atc_total_image_nav{float:left;padding-left:20px}
>    #atc_total_images_info{float:left;padding:4px 10px;font-size:12px;}
> </style>
> <br /><br /><br /><br />
>  
> <div align="center">
>    <h1>Parse a Link Like Facebook with PHP and Jquery</h1>
>    <div id="atc_bar" align="center">
>       Paste Link Here: <input type="text" name="url" size="40" id="url" value="" />
>       <input type="button" name="attach" value="Parse" id="attach" />
>       <input type="hidden" name="cur_image" id="cur_image" />
>       <div id="loader">
>  
>          <div align="center" id="atc_loading" style="display:none"><img src="load.gif" alt="Loading" /></div>
>          <div id="attach_content" style="display:none">
>             <div id="atc_images"></div>
>             <div id="atc_info">
>  
>                <label id="atc_title"></label>
>                <label id="atc_url"></label>
>                <br clear="all" />
>                <label id="atc_desc"></label>
>                <br clear="all" />
>             </div>
>             <div id="atc_total_image_nav" >
>                <a href="#" id="prev"><img src="prev.png"  alt="Prev" border="0" /></a><a href="#" id="next"><img src="next.png" alt="Next" border="0" /></a>
>             </div>
>  
>             <div id="atc_total_images_info" >
>                Showing <span id="cur_image_num">1</span> of <span id="atc_total_images">1</span> images
>             </div>
>             <br clear="all" />
>          </div>
>       </div>
>       <br clear="all" />
>    </div>
> </div>
> ```

> [!NOTE]
> ### JAVASCRIPT
> ```
> <script>
>  
>    $(document).ready(function(){
>  
>       // delete event
>       $('#attach').bind("click", parse_link);
>  
>       function parse_link ()
>       {
>          if(!isValidURL($('#url').val()))
>          {
>             alert('Please enter a valid url.');
>             return false;
>          }
>          else
>          {
>             $('#atc_loading').show();
>             $('#atc_url').html($('#url').val());
>             $.post("fetch.php?url="+escape($('#url').val()), {}, function(response){
>  
>                //Set Content
>                $('#atc_title').html(response.title);
>                $('#atc_desc').html(response.description);
>                $('#atc_price').html(response.price);
>  
>                $('#atc_total_images').html(response.total_images);
>  
>                $('#atc_images').html(' ');
>                $.each(response.images, function (a, b)
>                {
>                   $('#atc_images').append('<img src="'+b.img+'" width="100" id="'+(a+1)+'">');
>                });
>                $('#atc_images img').hide();
>  
>                //Flip Viewable Content
>                $('#attach_content').fadeIn('slow');
>                $('#atc_loading').hide();
>  
>                //Show first image
>                $('img#1').fadeIn();
>                $('#cur_image').val(1);
>                $('#cur_image_num').html(1);
>  
>                // next image
>                $('#next').unbind('click');
>                $('#next').bind("click", function(){
>  
>                   var total_images = parseInt($('#atc_total_images').html());
>                   if (total_images > 0)
>                   {
>                      var index = $('#cur_image').val();
>                      $('img#'+index).hide();
>                      if(index < total_images)
>                      {
>                         new_index = parseInt(index)+parseInt(1);
>                      }
>                      else
>                      {
>                         new_index = 1;
>                      }
>  
>                      $('#cur_image').val(new_index);
>                      $('#cur_image_num').html(new_index);
>                      $('img#'+new_index).show();
>                   }
>                });
>  
>                // prev image
>                $('#prev').unbind('click');
>                $('#prev').bind("click", function(){
>  
>                   var total_images = parseInt($('#atc_total_images').html());
>                   if (total_images > 0)
>                   {
>                      var index = $('#cur_image').val();
>                      $('img#'+index).hide();
>                      if(index > 1)
>                      {
>                         new_index = parseInt(index)-parseInt(1);;
>                      }
>                      else
>                      {
>                         new_index = total_images;
>                      }
>  
>                      $('#cur_image').val(new_index);
>                      $('#cur_image_num').html(new_index);
>                      $('img#'+new_index).show();
>                   }
>                });
>             });
>          }
>       };
>    });
>  
>    function isValidURL(url)
>    {
>       var RegExp = /(ftp|http|https):\/\/(\w+:{0,1}\w*@)?(\S+)(:[0-9]+)?(\/|\/([\w#!:.?+=&%@!\-\/]))?/;
>  
>       if(RegExp.test(url)){
>          return true;
>       }else{
>          return false;
>       }
>    }
> </script>
> ```
>

> [!NOTE]
> ### php
> ```
> $url = urldecode($_REQUEST['url']);
> $url = checkValues($url);
> $return_array = array();
>  
> $base_url = substr($url,0, strpos($url, "/",8));
> $relative_url = substr($url,0, strrpos($url, "/")+1);
>  
> // Get Data
> $cc = new cURL();
> $string = $cc->get($url);
> $string = str_replace(array("\n","\r","\t",'</span>','</div>'), '', $string);
>  
> $string = preg_replace('/(<(div|span)\s[^>]+\s?>)/',  '', $string);
> if (mb_detect_encoding($string, "UTF-8") != "UTF-8")
>    $string = utf8_encode($string);
>  
> // Parse Title
> $nodes = extract_tags( $string, 'title' );
> $return_array['title'] = trim($nodes[0]['contents']);
>  
> // Parse Base
> $base_override = false;
> $base_regex = '/<base[^>]*'.'href=[\"|\'](.*)[\"|\']/Ui';
> preg_match_all($base_regex, $string, $base_match, PREG_PATTERN_ORDER);
> if(strlen($base_match[1][0]) > 0)
> {
>    $base_url = $base_match[1][0];
>    $base_override = true;
> }
>  
> // Parse Description
> $return_array['description'] = '';
> $nodes = extract_tags( $string, 'meta' );
> foreach($nodes as $node)
> {
>    if (strtolower($node['attributes']['name']) == 'description')
>       $return_array['description'] = trim($node['attributes']['content']);
> }
>  
> // Parse Images
> $images_array = extract_tags( $string, 'img' );
> $images = array();
> for ($i=0;$i<=sizeof($images_array);$i++)
> {
>    $img = trim(@$images_array[$i]['attributes']['src']);
>    $width = preg_replace("/[^0-9.]/", '', $images_array[$i]['attributes']['width']);
>    $height = preg_replace("/[^0-9.]/", '', $images_array[$i]['attributes']['height']);
>  
>    $ext = trim(pathinfo($img, PATHINFO_EXTENSION));
>  
>    if($img && $ext != 'gif')
>    {
>       if (substr($img,0,7) == 'http://')
>          ;
>       else  if (substr($img,0,1) == '/' || $base_override)
>          $img = $base_url . $img;
>       else
>          $img = $relative_url . $img;
>  
>       if ($width == '' && $height == '')
>       {
>          $details = @getimagesize($img);
>  
>          if(is_array($details))
>          {
>             list($width, $height, $type, $attr) = $details;
>          }
>       }
>       $width = intval($width);
>       $height = intval($height);
>  
>       if ($width > 199 || $height > 199 )
>       {
>          if (
>             (($width > 0 && $height > 0 && (($width / $height) < 3) && (($width / $height) > .2))
>                || ($width > 0 && $height == 0 && $width < 700)
>                || ($width == 0 && $height > 0 && $height < 700)
>             )
>             && strpos($img, 'logo') === false )
>          {
>             $images[] = array("img" => $img, "width" => $width, "height" => $height, 'area' =>  ($width * $height),'offset' => $images_array[$i]['offset']);
>          }
>       }
>  
>    }
> }
> $return_array['images'] = array_values(($images));
> $return_array['total_images'] = count($return_array['images']);
>  
> header('Cache-Control: no-cache, must-revalidate');
> header('Expires: Mon, 26 Jul 1997 05:00:00 GMT');
> header('Content-type: application/json');
>  
> echo json_encode($return_array);
> exit;
> ```
> 

## https://twitter.com/share?url=https://www.redsunsoft.com/2011/01/parse-link-like-facebook-with-jquery-and-php/