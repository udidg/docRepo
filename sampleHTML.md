<!doctype html>
<html lang="en-US">
<head>
  <meta charset="utf-8"/>
  <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1"/>
  <link rel="stylesheet" type="text/css" href="http://nshipster.com/css/screen.css"/>
  <meta property="nshipster:hide-single-lang" content="swift,objective-c"/>
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.1.1/jquery.min.js"></script>
</head>

<body itemscope itemtype="http://schema.org/WebPage">

<div class="highlight"><pre><code class="language-swift" data-lang="swift"><span class="k">import</span> <span class="n">UIKit</span>

<span class="k">let</span> <span class="n">str</span> <span class="o">=</span> <span class="s">&quot;hipstar&quot;</span>
<span class="k">let</span> <span class="n">textChecker</span> <span class="o">=</span> <span class="bp">UITextChecker</span><span class="p">()</span>


</code></pre></div><div class="highlight"><pre><code class="language-objective-c" data-lang="objective-c"><span class="bp">NSString</span> <span class="o">*</span><span class="n">str</span> <span class="o">=</span> <span class="s">@&quot;hipstar&quot;</span><span class="p">;</span>
<span class="bp">UITextChecker</span> <span class="o">*</span><span class="n">textChecker</span> <span class="o">=</span> <span class="p">[[</span><span class="bp">UITextChecker</span> 

  </div>



</body>

  <script>
    if (window.navigator && window.navigator.loadPurpose === "preview") {
      window.location.href = "http://nshipster.com/topsites_preview.html";
    }
  </script>

  <script async>
    var Swiftype = window.Swiftype || {};
    (function() {
      Swiftype.key = 'Q5jNBiR8qVs5xE5dNect';
      var script = document.createElement('script');
      script.type = 'text/javascript';
      script.async = true;
      var entry = document.getElementsByTagName('script')[0];
      document.getElementsByTagName('script')[0].parentNode.insertBefore(script, entry);
    }());
  </script>

  <script>
    (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
    (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
    m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
    });
  </script>

<script>

$(document).ready(function() {
  var group = [];
  $('.highlight').each(function() {
      group.push($(this));

      if(!$(this).next().hasClass('highlight')) {
        var container = $('<div class="highlight-group"></div>');
        container.insertBefore(group[0]);

        for (i in group) {
            group[i].appendTo(container);
        }

        group = [];
      }
  });
  
  var hiddenSingleLanguages = $("meta[property='nshipster:hide-single-lang']").attr('content').split(',');
  
  $('.highlight-group').each(function() {
    var languages = [];
    $(this).find($("code")).each(function() {
      languages.push($(this).data('lang'));
    });

    if ((languages.length == 1) && (hiddenSingleLanguages.indexOf(languages[0].toLowerCase()) != -1)) {
        return;
    }
    
    $(this).children('.highlight:not(:first-child)').hide();

    var span = $('<span class="language-toggle"></span>');
    for (i in languages) {
      var language = languages[i];
      var a = $('<a data-lang="' + language + '">' + language.toProperCase() + '</a>');
      if (i == 0) {
        a.addClass('active');
      }
      span.append(a);
    }

    $(this).prepend(span);
  });


  var showAllWithLanguage = function(lang) {
    $('a[data-lang=' + lang + ']').each( function() {
      $(this).siblings('a').removeClass('active');
      $(this).addClass('active');
      $(this).parent().siblings('.highlight').each(function() {
        if ($(this).find('code').data('lang') === lang) {
          $(this).show();
        } else {
          $(this).hide()
        }
      });
    });
  };

  $('a[data-lang]').on('click', function() {
    var lang = $(this).data('lang');
    showAllWithLanguage(lang);
  });
  
});

String.prototype.toProperCase = function() {
  switch (this.toLowerCase()) {
    case 'json': return 'JSON';
    case 'javascript': return 'JavaScript';
    default: return this.replace(/\b\w+/g, function(txt) { return txt.charAt(0).toUpperCase() + txt.substr(1).toLowerCase(); })
  }
};

// Zepto.cookie plugin
// 
// Copyright (c) 2010, 2012 
// @author Klaus Hartl (stilbuero.de)
// @author Daniel Lacy (daniellacy.com)
// 
// Dual licensed under the MIT and GPL licenses:
// http://www.opensource.org/licenses/mit-license.php
// http://www.gnu.org/licenses/gpl.html
;(function($){
    $.extend($.fn, {
cookie : function (key, value, options) {
var days, time, result, decode
// A key and value were given. Set cookie.
if (arguments.length > 1 && String(value) !== "[object Object]") {
// Enforce object
                options = $.extend({}, options)
if (value === null || value === undefined) options.expires = -1
if (typeof options.expires === 'number') {
                    days = (options.expires * 24 * 60 * 60 * 1000)
                    time = options.expires = new Date()
                    time.setTime(time.getTime() + days)
                }
                value = String(value)
return (document.cookie = [
                    encodeURIComponent(key), '=',
                    options.raw ? value : encodeURIComponent(value),
                    options.expires ? '; expires=' + options.expires.toUTCString() : '',
                    options.path ? '; path=' + options.path : '',
                    options.domain ? '; domain=' + options.domain : '',
                    options.secure ? '; secure' : ''
                ].join(''))
            }
// Key and possibly options given, get cookie
            options = value || {}
            decode = options.raw ? function (s) { return s } : decodeURIComponent
return (result = new RegExp('(?:^|; )' + encodeURIComponent(key) + '=([^;]*)').exec(document.cookie)) ? decode(result[1]) : null
        }
    })
})
</script>


</html>

