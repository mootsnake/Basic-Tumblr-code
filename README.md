<--# Basic-Tumblr-code
The basic default tumblr theme. Adjusting for coding practice. I do not own.-->
<!DOCTYPE html>
<html>
    <head>
        <title>{Title}{block:SearchPage} ({lang:Search results for SearchQuery}){/block:SearchPage}{block:PermalinkPage}{block:PostSummary} — {PostSummary}{/block:PostSummary}{/block:PermalinkPage}</title>

        <meta charset="utf-8">
        <meta name="description" content="{block:IndexPage}{block:Description}{MetaDescription}{/block:Description}{/block:IndexPage}{block:PermalinkPage}{block:PostSummary}{PostSummary}{/block:PostSummary}{/block:PermalinkPage}" />

        <meta name="color:Accent" content="#4EA3D0"/>
        <meta name="font:Body" content="'Helvetica Neue', Helvetica, Arial, sans-serif"/>
        <meta name="if:Two column posts" content="1"/>

        <!-- Appearance option -->
        <meta name="if:Show bar on top" content="1"/>
        <meta name="if:Show blog title" content="1"/>
        <meta name="if:Show blog description" content="1"/>
        <meta name="if:Show profile photo" content="1"/>
        <meta name="if:Use endless scrolling" content="1"/>


        <meta name="if:Show right column" content="1"/>
        <meta name="if:Place timestamp in left column" content="1"/>
        <meta name="if:Use larger font for quotes" content="0"/>
        <meta name="if:Show image shadows" content="1"/>
        <meta name="if:Show tags" content="1"/>
        <meta name="if:Show post notes" content="1"/>
        <meta name="if:Show copyright in footer" content="1"/>
        <meta name="text:Disqus Shortname" content="" />
        <meta name="text:Google Analytics ID" content=""/>

        <link rel="shortcut icon" href="{Favicon}" />
        <link rel="alternate" type="application/rss+xml" title="RSS" href="{RSS}"/>

        <!-- HTML5 Shiv -->
        <!--[if lt IE 9]>
                <script src="http://static.tumblr.com/hriofhd/Qj0m8pn7q/html5shiv.js"></script>
        <![endif]-->

        <!-- Reset CSS -->
        <link rel="stylesheet" href="http://static.tumblr.com/thpaaos/DIcklyl4z/reset.css" type="text/css">

        <!-- Theme CSS -->
        <style type="text/css" media="screen">
            body {
                -webkit-font-smoothing: antialiased;
                font-size: 15px;
                font-family: 'Helvetica Neue', Helvetica, Arial, sans-serif;
                line-height: 24px;
                margin: 0;
                padding: 0;
            }

            *:active, *:focus { outline-width: 0px; }
            img { max-width: 100% }
            .post .top.media img { width: 100%; }
            a { text-decoration: none; color: {Color:Accent}; }
            a img { border-width: 0px; }
            strong { font-weight: bold; }
            em { font-style: italic; }

            .group:after {
                visibility: hidden;
                display: block;
                content: "";
                clear: both;
                height: 0;
                }
            * html .group             { zoom: 1; } /* IE6 */
            *:first-child+html .group { zoom: 1; } /* IE7 */

            iframe#tumblr_controls {
                top: 12px !important;
            }

            #color_bar {
                height: 12px;
                background: {Color:Accent};
            }

            #container {
                width: 950px;
                margin: 0 auto;
                padding: 60px 20px;
            }

            #header {
                height: 48px;
                margin: 0 0 60px 0;
            }

            #blog_info {
                width: 700px;
                margin: 0 60px 0 0;
                float: left;
            }

            #blog_info h1 {
                font-size: 36px;
                font-weight: bold;
                letter-spacing: -1px;
                line-height: 36px;
                margin: 8px 0 0 0;
            }

            #blog_info h1 a {
                color: #333333;
            }
                            
            #blog_info h1 a:hover {
                color: #000;
            }

            #blog_info h1 a:active {
                position: relative;
                top: 1px;
            }

            #blog_info p, #blog_info .cont {
                color: #646464;
                margin-top: 7px;
            }

            .cont {
                margin-bottom: 7px;
            }

            #blog_avatar {
                width: 188px;
                position: relative;
                float: right;
                {block:IfNotShowBlogTitle}float: left;{/block:IfNotShowBlogTitle}
            }

            #blog_avatar a {
                width: 48px;
                height: 48px;
                {block:IfShowImageShadows}
                    -webkit-box-shadow: 0px 1px 3px rgba(0, 0, 0, .21);
                    box-shadow: 0px 1px 3px rgba(0, 0, 0, .21);
                {/block:IfShowImageShadows}  
                position: absolute;
                top: 0;
                left: 0;
                display: block;
            }

            #blog_avatar img {
                width: 48px;
                -webkit-border-radius: 2px;
                -moz-border-radius: 2px;
                border-radius: 2px;
            }

            #blog_avatar a::before {
                content: " ";
                width: 46px;
                height: 46px;
                -webkit-border-radius: 2px;
                -moz-border-radius: 2px;
                border-radius: 2px;
                border: 1px solid rgba(0,0,0,.1);
                position: absolute;
                top: 0px;
                left: 0px;
                z-index: 999;
                display: block;
            }

            #blog_avatar:hover a {
                width: 64px;
                height: 64px;
                top: -8px;
                left: -8px;
            }

            #blog_avatar:hover a img {
                width: 64px;
            }

            #blog_avatar:hover a::before {
                width: 62px;
                height: 62px;
            }

            #blog_avatar:active a {
                top: -7px;
                -webkit-box-shadow: 0px 0px 1px rgba(0, 0, 0, .21);
                box-shadow: 0px 0px 1px rgba(0, 0, 0, .21);
            }

            #posts {
                width: 700px;
                color: #4C4C4C;
                margin: 0 60px 0 0;
                float: left;
            }

            #posts .post {
                list-style-type: none;
                border-bottom: 1px solid #E6E6E6;
                margin: 0 0 45px 0;
                padding: 0 0 45px 0;
            }

{block:IfDisqusShortname}
            #posts .post #disqus_thread {
                border-top: 1px solid #E6E6E6;
                margin: 20px 0 0 0;
                padding: 25px 0 0 0;
            }

            #posts .post .caption a.disquscomments {
                font-size: 12px;
                font-family: 'Times New Roman', Times, serif;
                letter-spacing: 2px;
                text-transform: uppercase;
                -webkit-font-smoothing: subpixel-antialiased;
            }
{/block:IfDisqusShortname}

            .top.audio * {
                width: 700px;
                height: 91px
            }

            .top.media {
                line-height: 0;
                {block:IfShowImageShadows}
                    -webkit-box-shadow: 0px 2px 7px 0px rgba(0, 0, 0, .27);
                    box-shadow: 0px 2px 7px 0px rgba(0, 0, 0, .27);
                {/block:IfShowImageShadows}
                position: relative;
                display: inline-block;
            }

            .top.media.photoset {
                line-height: 0;
                {block:IfShowImageShadows}
                    -webkit-box-shadow: none;
                    box-shadow: none;
                {/block:IfShowImageShadows}
                position: relative;
                display: inline-block;
            }

            .media img {
                -webkit-border-radius: 2px;
                -moz-border-radius: 2px;
                border-radius: 2px;
            }

            .link_post .link {
                color: {Color:Accent};
                font-size: 21px;
                font-weight: bold;
                border: 1px solid rgba({RGBcolor:Accent}, 0.13);
                background: rgba({RGBcolor:Accent}, 0.13);
                -webkit-border-radius: 2px;
                -moz-border-radius: 2px;
                border-radius: 2px;
                padding: 15px 53px 15px 20px;
                position: relative;
                display: block;
            }

            .link .arrow {
                width: 0; 
                height: 0; 
                border-top: 8px solid transparent;
                border-bottom: 8px solid transparent;
                border-left: 12px solid {Color:Accent};
                position: absolute;
                top: 50%;
                right: 20px;
                margin-top: -8px;
                display: block;
            }

            .link_post .link:hover {
                border: 1px solid rgba({RGBcolor:Accent}, 0.2);
                background: rgba({RGBcolor:Accent}, 0.2);
            }

            .link_post .link:active {
                position: relative;
                top: 1px;
            }

            #posts .post .caption_and_post_info.after_top_part {
                border-top: 0;
                margin: 30px auto auto auto;
                padding-top: 0;
            }

            .post .caption {
                width: auto;
                float: none;
            }

            {block:IfPlaceTimestampInLeftColumn}
            .post .caption {
                width: 513px;
                float: right;
            }
            {/block:IfPlaceTimestampInLeftColumn}

            .content_source {
                margin-bottom: 20px;
            }

            .content_source img {
                margin: 0 0 0 4px !important;
                opacity: 0.7;
                vertical-align: middle;
            }

            .caption a, .description a {
                color: {Color:Accent};
                padding: 0 1px;
            }

            .caption a:hover, .description a:hover {
                background: rgba({RGBcolor:Accent}, 0.13);
            }

            .caption a:active, .description a:active {
                background: rgba({RGBcolor:Accent}, 0.2);
            }

            .caption h2 {
                font-size: 32px;
                line-height: 33px;
                margin: 0 0 18px 0;
            }

            .caption h2 a {
                color: #333;
                font-weight: bold;
                letter-spacing: -1px;
            }

            .caption h2 a:hover {
                color: {Color:Accent};
                background: transparent;
            }
                                
            .caption blockquote {
                border-left: 2px solid #E6E6E6;
                padding: 1px 0 1px 20px;
            }

            .caption pre {
                background: #eee;
                font-family: Consolas, Menlo, Monaco, "Lucida Console", "Liberation Mono", "DejaVu Sans Mono", "Bitstream Vera Sans Mono", "Anonymous Pro", "Courier New", monospace, serif;
                overflow: scroll;
                padding: 10px;
                border-radius: 3px;
                font-size: 13px;
                line-height: 19px;
            }

            .caption p,
            .caption ol,
            .caption ul,
            .caption pre,
            .caption h1,
            .caption h2,
            .post h3,
            .caption h4,
            .caption h5,
            .caption blockquote,
            .caption img,
            .caption embed,
            .caption object {
                margin: 0 0 20px 0;
            }

            .caption p:empty {
                display: none;
            }

            .caption iframe {
                display: block !important;
            }

            .post .caption ul,
            .post .caption ol {
                margin-left: 18px;
            }

            .caption .question {
                display: block;
                padding: 15px;
                font-size: 15px;
            }

            .caption .answer {
                margin-top: 20px;
            }

            .caption .asker {
                line-height: 24px;
                margin: 25px 20px 0 23px;
            }

            .caption .asker img {
                float: left;
                margin: 0 7px 0 0;
            }

            .caption .asker a {
                margin-left: 0;
            }

            .caption .quote {
                color: #333;
                font-weight: bold;
            }

            .quote span {
                display: inline-block;
            }

            .quote.short_text {
                font-size: 50px;
                letter-spacing: -2px;
                line-height: 48px;
                margin: 0 0 18px 0;
            }

            .quote.short_text span {
                margin: 0 0 0 -22px;
            }

            .quote.medium_text {
                font-size: 36px;
                letter-spacing: -1px;
                line-height: 36px;
                margin: 0 0 20px 0;
            }

            .quote.medium_text span {
                margin: 0 0 0 -13px;
            }

            .quote.long_text,
            .quote.text {
                font-size: 24px;
                line-height: 27px;
                margin: 0 0 20px 0;
            }

            .quote.long_text span {
                margin: 0 0 0 -9px;
            }

            .quote.larger_text {
                font-size: 50px !important;
                letter-spacing: -2px !important;
                line-height: 48px !important;
                margin: 0 0 18px 0 !important;
            }

            .quote.larger_text span {
                margin: 0 0 0 -22px !important;
            }

            .quote_source {
                margin: 0 0 20px 0 !important;
            }

            .caption .conversation {
                margin-left: 0 !important;
                margin-bottom: 30px;
                list-style-type: none;
            }

            .conversation .chat_line {
                padding: 10px 16px;
            }

            .conversation .chat_line.user1 {
                background: #f5f5f5;
            }

            .conversation .chat_line.user2 {
                background: #fff;
            }

            .conversation .chat_line.user3 {
                background: #ddd;
            }

            .conversation .chat_line.user4 {
                background: #ccc;
            }

            .post .post_info {
                width: auto;
                font-size: 12px;
                font-family: 'Times New Roman', Times, serif;
                letter-spacing: 2px;
                text-transform: uppercase;
                list-style-type: none;
                -webkit-font-smoothing: subpixel-antialiased;
                margin: 1px 0 0 -3px;
                overflow: hidden;
            }

            .post_info li {
                line-height: 14px;
                margin: 10px 0;
                float: left;
            }

            .post_info li a {
                margin: 0 10px 0 0;
                padding: 0 2px 0 5px;
            }

            .post_info .timestamp {
                color: #4c4c4c;
                padding: 0 2px 0 5px;
                display: inline-block;
            }

            .post_info .timestamp:hover {
                background: rgba(0,0,0,.08);
            }

            .post_info .timestamp:active {
                background: rgba(0,0,0,.1);
            }

            .post_info .notecount {
                color: #4c4c4c;
                padding: 0 2px 0 5px;
                display: inline-block;
            }

            .post_info .notecount:hover {
                background: rgba(0,0,0,.08);
            }

            .post_info .notecount:active {
                background: rgba(0,0,0,.1);
            }
            
            /* Post controls */

            .post_controls {
                border: 1px solid #e8e8e8;
                border-radius: 3px;
                float: left;
                list-style: none;
                margin: -10px 15px 15px 0;
            }
    
            /* requires high specificity */
            .post .post_info .post_controls li,
            .post .post_info.floating .post_controls li {
                float: left;
                margin: 0;
                padding: 7px 15px;
                height: 21px;
            }

            .post_controls li:first-child {
                border-right: 1px solid #e8e8e8;
            }

            .post .post_info .post_controls li a,
            .post .post_info.floating .post_controls li a {
                margin: 0;
                padding: 0;
            }
            

            /* Baselines */

            .tag {
                color: {Color:Accent};
                display: table;
            }

            .tag span {
                color: #4c4c4c;
                display: table-cell;
            }

            .tag:hover {
                background: rgba({RGBcolor:Accent}, 0.13);
            }

            .tag:hover span {
                color: {Color:Accent};
            }

            .tag:active {
                background: rgba({RGBcolor:Accent}, 0.2);
            }

            .post .post_info.floating {
                width: 157px;
                float: left;
            }

            .post .post_info.floating li {
                float: none;
            }

            .post_notes {
                clear: both;
            }

            ol.notes {
                color: #4C4C4C;
                font-size: 13px;
                text-shadow: 0px 1px 0px rgba(255,255,255,.7);
                text-align: left;
                list-style-type: none;
                border-top: solid 1px #E6E6E6;
                -webkit-font-smoothing: subpixel-antialiased !important;
                margin: 40px auto auto auto;
            }

            ol.notes li.note {
                border-bottom: solid 1px #E6E6E6;
                padding: 9px 0 10px 0;
            }

            ol.notes li.note img.avatar {
                width: 16px;
                height: 16px;
                border-radius: 3px;
                vertical-align: -4px;
                margin-right: 6px;
            }

            ol.notes a {
                color: #4C4C4C;
                text-decoration: underline;
            }

                ol.notes a:hover {
                    color: #4C4C4C;
                }

            ol.notes li.note blockquote {
                border-color: #eee;
                padding: 4px 10px;
                margin: 10px 0px 0px 25px;
            }

            ol.notes li.note blockquote a {
                text-decoration: none;
            }

            ol.notes li.note:last-child {
                border-width: 0px;
            }

            #sidebar {
                width: 188px;
                color: #4c4c4c;
                font-size: 14px;
                margin: -8px 0 0 0;
                float: right;
            }

            #sidebar .description {
                line-height: 21px;
                border-bottom: 1px solid #E6E6E6;
                margin: 3px 0 20px 0;
                padding: 0 0 20px 0;
            }

            #sidebar .links {
                font-size: 12px;
                font-family: 'Times New Roman', Times, serif;
                letter-spacing: 2px;
                text-transform: uppercase;
                list-style-type: none;
                -webkit-font-smoothing: subpixel-antialiased;
                margin: 0 0 20px 0;
                line-height: 20px;
            }

            #sidebar .links a {
                color: #4c4c4c;
            }

            #sidebar .links a:hover {
                color: {Color:Accent};
            }

            .links .icon {
                width: 12px;
                height: 12px;
                background: #383838 url('http://static.tumblr.com/thpaaos/1xRm66voi/icons_sprite.png');
                margin: 0 8px 0 0;
                display: inline-block;
            }

            .links a:hover .icon {
                background-color: {Color:Accent};
            }

            .ask .icon { background-position: 0 0; margin-bottom: -2px; }
            .submit .icon { background-position: 0 -12px; margin-bottom: -1px; }
            .rss .icon { background-position: 0 -24px; }
            .archive .icon { background-position: 0 -36px; }

            .bubble {
                color: #6f6f6f;
                font-size: 13px;
                line-height: 20px;
                background: #f5f5f5;
                border: 1px solid #d5d5d5;
                -webkit-border-radius: 4px;
                -moz-border-radius: 4px;
                border-radius: 4px;
                padding: 8px 12px;
                position: relative;
                display: none;
            }

            #twitter_container .bubble:first-child {
                display: block;
            }

            .bubble .arrow {
                width: 0; 
                height: 0; 
                position: absolute;
                display: block;
            }

            .bubble .arrow.fill {
                border-left: 8px solid transparent;
                border-right: 8px solid transparent;
                border-top: 8px solid #f5f5f5;
                bottom: -8px;
                left: 25px;
            }

            .bubble .arrow.border {
                border-left: 10px solid transparent;
                border-right: 10px solid transparent;
                border-top: 10px solid #d5d5d5;
                bottom: -10px;
                left: 23px;
            }

            .bubble:hover {
                background: #f2f2f2;
                border-color: #CFCFCF;
            }

            .bubble:hover .arrow.fill {
                border-top-color: #F1F1F1;
            }

            .bubble:hover .arrow.border {
                border-top-color: #d5d5d5;
            }

            .twitter_username {
                max-width: 166px;
                color: #4c4c4c;
                font-size: 12px;
                font-family: 'Times New Roman', Times, serif;
                letter-spacing: 0.4em;
                text-transform: uppercase;
                text-overflow: ellipsis;
                -webkit-font-smoothing: subpixel-antialiased;
                margin: 11px 0 0 22px;
                overflow: hidden;
                display: inline-block;
                opacity: 1;
            }

            .twitter_username:hover {
                color: {Color:Accent};
            }

            #footer {
                width: 700px;
                color: #4C4C4C;
                font-size: 12px;
                font-family: 'Times New Roman', Times, serif;
                letter-spacing: 2px;
                text-transform: uppercase;
                -webkit-font-smoothing: subpixel-antialiased;
            }

            #footer .copyright {
                width: 50%;
                float: left;
            }

            #footer .pagination {
                width: 230px;
                text-align: right;
                float: right;
                position: relative;
            }

            .pagination .count {
                float: left;
            }

            .pagination .buttons {
                width: 113px;
                height: 30px;
                margin: -2px 0 0 30px;
                float: right;
                position: absolute;
                top: 0;
                right: 0;
                z-index: 10;
            }

            .pagination .buttons.disabled {
                z-index: 9;
            }

            .buttons a,
            .buttons li {
                width: 56px;
                height: 28px;
                line-height: 999px;
                text-align: center;
                border: 1px solid #C8C8C8;
                -webkit-box-shadow: inset 0px 1px 0px 0px rgba(255, 255, 255, 1);
                box-shadow: inset 0px 1px 0px 0px rgba(255, 255, 255, 1);
                background: #f1f1f1; /* Old browsers */
                background: -moz-linear-gradient(top,  #f1f1f1 0%, #e8e8e8 100%); /* FF3.6+ */
                background: -webkit-gradient(linear, left top, left bottom, color-stop(0%,#f1f1f1), color-stop(100%,#e8e8e8)); /* Chrome,Safari4+ */
                background: -webkit-linear-gradient(top,  #f1f1f1 0%,#e8e8e8 100%); /* Chrome10+,Safari5.1+ */
                background: -o-linear-gradient(top,  #f1f1f1 0%,#e8e8e8 100%); /* Opera 11.10+ */
                background: -ms-linear-gradient(top,  #f1f1f1 0%,#e8e8e8 100%); /* IE10+ */
                background: linear-gradient(top,  #f1f1f1 0%,#e8e8e8 100%); /* W3C */
                filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#f1f1f1', endColorstr='#e8e8e8',GradientType=0 );/* IE6-9 */
                list-style-type: none;
                overflow: hidden;
                position: relative;
                display: block;
            }

            .buttons.disabled li {
                background: #f5f5f5;
            }

            .buttons a:active {
                -webkit-box-shadow: none;
                box-shadow: none;
                background: #E6E6E6;
            }

            .buttons .arrow {
                width: 10px;
                height: 14px;
                position: absolute;
                top: 50%;
                display: block;
                background-image: url(http://static.tumblr.com/ogedyaw/xu1m8jxnf/arrow_sprite.png);
            }

            .buttons .left {
                -webkit-border-top-left-radius: 2px;
                -webkit-border-bottom-left-radius: 2px;
                -moz-border-radius-topleft: 2px;
                -moz-border-radius-bottomleft: 2px;
                border-top-left-radius: 2px;
                border-bottom-left-radius: 2px;
                position: absolute;
                left: 0;
            }

            .left .arrow {
                background-position: 0 15px;
                margin: -7px auto auto 20px;
            }
                
            .disabled .left .arrow {
                background-position: 0 0;
            }

            .buttons .right {
                border-left-width: 1px;
                -webkit-border-top-right-radius: 2px;
                -webkit-border-bottom-right-radius: 2px;
                -moz-border-radius-topright: 2px;
                -moz-border-radius-bottomright: 2px;
                border-top-right-radius: 2px;
                border-bottom-right-radius: 2px;
                position: absolute;
                right: 0;
            }

            .right .arrow {
                background-position: 10px -71px;
                margin: -7px auto auto 24px;
            }

            .disabled .right .arrow {
                background-position: 10px -56px;
            }

            /* Protection for parents that have floating children */
            #header:after,
            #container:after,
            .caption_and_post_info:after,
            #footer:after
            .buttons:after {
                content: ".";
                display: block;
                height: 0;
                clear: both;
                visibility: hidden;
            }
        </style>

        {block:PermalinkPage}
            <!-- Simplified permalink pages (Hides right column) -->
            <style type="text/css" media="screen">
                #container {
                    width: 700px;
                }

                #header {
                    width: 700px;
                }

                #blog_info {
                    width: 513px;
                    margin: 0;
                }

                #blog_avatar {
                    width: 48px;
                    height: 48px;
                    backround-color: red;
                }

                #blog_avatar a {
                    position: absolute;
                    left: auto;
                    right: 0;
                }

                #blog_avatar:hover a {
                    left: auto;
                    right: -8px;
                }

                #sidebar {
                    display: none;
                }

                #blog_info {
                    {block:IfNotShowBlogTitle}
                        width: 632px;
                        margin-top: -7px;
                        float: right;
                    {/block:IfNotShowBlogTitle}
                }

                #blog_info .description {
                    margin-bottom: 60px;
                }

                .post .post_info,
                .post .post_info.floating,
                .post .caption {
                    width: auto !important;
                    float: none;
                }

                .post .post_info {
                    margin-top: 45px;
                }

                .post .post_info li,
                .post .post_info.floating li {
                    line-height: 14px;
                    margin-bottom: 10px;
                    float: left;
                }

                .post .post_info li a,
                .post .post_info.floating li a {
                    margin: 0 10px 0 0;
                    padding: 0 2px 0 5px;
                }
            </style>
        {block:PermalinkPage}

        {block:IfNotShowRightColumn}
            <!-- Hides right column -->
            <style type="text/css" media="screen">
                #container {
                    width: 700px;
                }

                #header {
                    width: 700px;
                }

                #blog_info {
                    width: 513px;
                    margin: 0;
                }

                #blog_avatar {
                    width: 48px;
                    height: 48px;
                    backround-color: red;
                }

                #blog_avatar a {
                    position: absolute;
                    left: auto;
                    right: 0;
                }

                #blog_avatar:hover a {
                    left: auto;
                    right: -8px;
                }

                #sidebar {
                    display: none;
                }

                #blog_info {
                    {block:IfNotShowBlogTitle}
                        width: 632px;
                        margin-top: -7px;
                        float: right;
                    {/block:IfNotShowBlogTitle}
                }

                #blog_info .description {
                    margin-bottom: 60px;
                }

                .post .post_info,
                .post .post_info.floating,
                .post .caption {
                    width: auto !important;
                    float: none;
                }

                .post .post_info {
                    margin-top: 45px;
                }

                .post .post_info li,
                .post .post_info.floating li {
                    line-height: 14px;
                    margin-bottom: 10px;
                    float: left;
                }

                .post .post_info li a,
                .post .post_info.floating li a {
                    margin: 0 10px 0 0;
                    padding: 0 2px 0 5px;
                }
            </style>
        {/block:IfNotShowRightColumn}

        <!-- Custom CSS -->
        <style type="text/css" media="screen">
            {CustomCSS}
        </style>

    </head>
    <body>
        {block:IfShowBarOnTop}<section id="color_bar"></section>{/block:IfShowBarOnTop}

        <section id="container" class="group">            
            <header id="header">
                <section id="blog_info">
                    {block:IfShowBlogTitle}<h1><a href="/">{Title}</a></h1>{/block:IfShowBlogTitle}
                    {block:PermalinkPage}{block:IfShowBlogDescription}{block:Description}<div class="description cont">{Description}</div>{/block:Description}{/block:IfShowBlogDescription}{/block:PermalinkPage}
                    {block:IfNotShowRightColumn}{block:IfShowBlogDescription}<div class="cont description"{block:PermalinkPage} style="display:none"{/block:PermalinkPage}>{Description}</div>{/block:IfShowBlogDescription}{/block:IfNotShowRightColumn}
                </section>

                {block:IfShowProfilePhoto}
                    <section id="blog_avatar">
                        <a href="/" class="avatar"><img src="{PortraitURL-64}"></a>
                    </section>
                {/block:IfShowProfilePhoto}
            </header>

            <aside id="sidebar">
                {block:IfShowBlogDescription}{block:Description}<div class="cont description group">{Description}</div>{/block:Description}{/block:IfShowBlogDescription}

                {block:HasPages}
                    <ul class="links">
                        {block:Pages}
                            <li><a href="{URL}">{Label}</a></li>
                        {/block:Pages}
                    </ul>
                {/block:HasPages}

                <ul class="links" style="display:none;{block:AskEnabled} display:block;{/block:AskEnabled}{block:SubmissionsEnabled} display:block;{/block:SubmissionsEnabled}">
                    {block:AskEnabled}<li><a href="/ask" class="ask"><span class="icon"></span>ask me anything</a></li>{/block:AskEnabled}
                    {block:SubmissionsEnabled}<li><a href="/submit" class="submit"><span class="icon"></span>submit a post</a></li>{/block:SubmissionsEnabled}
                </ul>

                <ul class="links">
                    <li><a href="{RSS}" class="rss"><span class="icon"></span>rss</a></li>
                    <li><a href="/archive" class="archive"><span class="icon"></span>archive</a></li>
                </ul>

                {block:Twitter}
                    <aside id="twitter_container" style="display:none"></aside>

                    <script type="text/javascript">
                        function recent_tweets(data) {
                            document.getElementById("twitter_container").innerHTML =
                            document.getElementById("twitter_container").innerHTML +
                            '<a class="bubble" href="http://twitter.com/{TwitterUsername}/status/' +
                            (data[0].id_str ? data[0].id_str : data[0].id) +
                            '">' + data[0].text +
                            '<span class="arrow border"></span><span class="arrow fill"></span></a>' +
                            '<a href="http://twitter.com/{TwitterUsername}" class="twitter_username">@{TwitterUsername}</a>';

                            document.getElementById("twitter_container").style.display = 'block';
                        }
                    </script>
                {/block:Twitter}
            </aside>

            <ul id="posts">
                <!-- START POSTS -->
                {block:Posts}

                        <li class="post group" {block:IfShowPostNotes} {block:PostNotes} style="padding:0"{/block:PostNotes} {/block:IfShowPostNotes}>  

                        {block:Photo}
                            <section class="top media" style="display:block;">
                                 {LinkOpenTag}<img src="{PhotoURL-HighRes}" alt="{PhotoAlt}"> {LinkCloseTag}{Question}
                            </section>
                        {/block:Photo}

                        {block:Photoset}
                            <section class="top media photoset">
                                {Photoset-700}
                            </section>
                        {/block:Photoset}

                        {block:Link}
                            <section class="top link_post">
                                <a href="{URL}" class="link">{Name}<span class="arrow"></span></a>
                            </section>
                        {/block:Link}

                        {block:Audio}
                            <section class="top audio">
                            {AudioPlayerBlack}
                            </section>
                        {/block:Audio}

                        {block:Video}
                            <section class="top media">
                                {Video-700}
                            </section>
                        {/block:Video}

                        <section class="group caption_and_post_info
                            {block:Photo} after_top_part isphoto{/block:Photo}
                            {block:Photoset} after_top_part isphoto{/block:Photoset}
                            {block:Link} after_top_part islink{/block:Link}
                            {block:Audio} after_top_part isaudio{/block:Audio}
                            {block:Video} after_top_part isvideo{/block:Video}
                        ">
                            {block:Text}
                                <section class="caption group">
                                    {block:Title}<h2><a href="{Permalink}">{Title}</a></h2>{/block:Title}
                                    <div class="cont group">{Body}</div>
                                    {block:ContentSource}
                                        <div class="cont content_source">
                                            <a href="{SourceURL}">
                                                {lang:Source}:
                                                {block:SourceLogo}
                                                    <img src="{BlackLogoURL}" width="{LogoWidth}" height="{LogoHeight}" alt="{SourceTitle}" />
                                                {/block:SourceLogo}
                                                {block:NoSourceLogo}
                                                    {SourceTitle}
                                                {/block:NoSourceLogo}
                                            </a>
                                        </div>
                                    {/block:ContentSource}
                                </section>
                            {/block:Text}

                            {block:Answer}
                                <section class="caption group">
                                    <div class="cont group">

                                        <div class="question bubble">
                                            {Question}
                                            <span class="arrow border"></span>
                                            <span class="arrow fill"></span>
                                        </div>
                                        <div class="asker group">
                                            <img src="{AskerPortraitURL-24}" width="24" height="24" /> {Asker}
                                        </div>
                                        <div class="answer cont">{Answer}</div>
                                    </div>
                                    {block:ContentSource}
                                        <div class="cont content_source">
                                            <a href="{SourceURL}">
                                                {lang:Source}:
                                                {block:SourceLogo}
                                                    <img src="{BlackLogoURL}" width="{LogoWidth}" height="{LogoHeight}" alt="{SourceTitle}" />
                                                {/block:SourceLogo}
                                                {block:NoSourceLogo}
                                                    {SourceTitle}
                                                {/block:NoSourceLogo}
                                            </a>
                                        </div>
                                    {/block:ContentSource}
                                </section>
                            {/block:Answer}
                            
                            {block:Photo}
                                <section class="caption group">
                                    {block:Caption}
                                        <div class="cont">{Caption}</div>
                                    {/block:Caption}
                                    {block:ContentSource}
                                        <div class="cont content_source">
                                            <a href="{SourceURL}">
                                                {lang:Source}:
                                                {block:SourceLogo}
                                                    <img src="{BlackLogoURL}" width="{LogoWidth}" height="{LogoHeight}" alt="{SourceTitle}" />
                                                {/block:SourceLogo}
                                                {block:NoSourceLogo}
                                                    {SourceTitle}
                                                {/block:NoSourceLogo}
                                            </a>
                                        </div>
                                    {/block:ContentSource}
                                </section>
                            {/block:Photo}

                            {block:Photoset}
                                <section class="caption group">
                                    {block:Caption}
                                        <div class="cont">{Caption}</div>
                                    {/block:Caption}
                                    {block:ContentSource}
                                        <div class="cont content_source">
                                            <a href="{SourceURL}">
                                                {lang:Source}:
                                                {block:SourceLogo}
                                                    <img src="{BlackLogoURL}" width="{LogoWidth}" height="{LogoHeight}" alt="{SourceTitle}" />
                                                {/block:SourceLogo}
                                                {block:NoSourceLogo}
                                                    {SourceTitle}
                                                {/block:NoSourceLogo}
                                            </a>
                                        </div>
                                    {/block:ContentSource}
                                </section>
                            {/block:Photoset}
                            
                            {block:Quote}
                                    <section class="caption group">
                                        <section class="quote {Length}_text {block:IfUseLargerFontForQuotes}larger_text{/block:IfUseLargerFontForQuotes}"><span>“</span>{Quote}”</section>
                                        {block:Source}
                                            <div class="cont quote_source">&mdash; {Source}</div>
                                        {/block:Source}
                                        {block:ContentSource}
                                            <div class="cont content_source">
                                                <a href="{SourceURL}">
                                                    {lang:Source}:
                                                    {block:SourceLogo}
                                                        <img src="{BlackLogoURL}" width="{LogoWidth}" height="{LogoHeight}" alt="{SourceTitle}" />
                                                    {/block:SourceLogo}
                                                    {block:NoSourceLogo}
                                                        {SourceTitle}
                                                    {/block:NoSourceLogo}
                                                </a>
                                            </div>
                                        {/block:ContentSource}
                                    </section>
                            {/block:Quote}
                            
                            {block:Link}
                                {block:Description}
                                    <section class="caption group">
                                        <div class="cont">{Description}</div>
                                        {block:ContentSource}
                                            <div class="cont content_source">
                                                <a href="{SourceURL}">
                                                    {lang:Source}:
                                                    {block:SourceLogo}
                                                        <img src="{BlackLogoURL}" width="{LogoWidth}" height="{LogoHeight}" alt="{SourceTitle}" />
                                                    {/block:SourceLogo}
                                                    {block:NoSourceLogo}
                                                        {SourceTitle}
                                                    {/block:NoSourceLogo}
                                                </a>
                                            </div>
                                        {/block:ContentSource}
                                    </section>
                                {/block:Description}
                            {/block:Link}
                            
                            {block:Chat}
                                <section class="caption group">
                                    {block:Title}<h2><a href="{Permalink}">{Title}</a></h2>{/block:Title}
                                    <ul class="conversation">
                                        {block:Lines}
                                            <li class="chat_line user{UserNumber}">
                                                {block:Label}
                                                    <strong>{Label}</strong>&nbsp;&nbsp;
                                                {/block:Label}
                                                {Line}
                                            </li>
                                        {/block:Lines}
                                    </ul>
                                    {block:ContentSource}
                                        <div class="cont content_source">
                                            <a href="{SourceURL}">
                                                {lang:Source}:
                                                {block:SourceLogo}
                                                    <img src="{BlackLogoURL}" width="{LogoWidth}" height="{LogoHeight}" alt="{SourceTitle}" />
                                                {/block:SourceLogo}
                                                {block:NoSourceLogo}
                                                    {SourceTitle}
                                                {/block:NoSourceLogo}
                                            </a>
                                        </div>
                                    {/block:ContentSource}
                                </section>
                            {/block:Chat}

                            {block:Audio}
                                {block:Caption}
                                    <section class="caption group">
                                        <div class="cont">{Caption}</div>
                                        {block:ContentSource}
                                            <div class="cont content_source">
                                                <a href="{SourceURL}">
                                                    {lang:Source}:
                                                    {block:SourceLogo}
                                                        <img src="{BlackLogoURL}" width="{LogoWidth}" height="{LogoHeight}" alt="{SourceTitle}" />
                                                    {/block:SourceLogo}
                                                    {block:NoSourceLogo}
                                                        {SourceTitle}
                                                    {/block:NoSourceLogo}
                                                </a>
                                            </div>
                                        {/block:ContentSource}
                                    </section>
                                {/block:Caption}
                            {/block:Audio}
                            
                            {block:Video}
                                <section class="caption group">
                                {block:Caption}
                                    <div class="cont">{Caption}</div>
                                {/block:Caption}
                                {block:ContentSource}
                                    <div class="cont content_source">
                                        <a href="{SourceURL}">
                                            {lang:Source}:
                                            {block:SourceLogo}
                                                <img src="{BlackLogoURL}" width="{LogoWidth}" height="{LogoHeight}" alt="{SourceTitle}" />
                                            {/block:SourceLogo}
                                            {block:NoSourceLogo}
                                                {SourceTitle}
                                            {/block:NoSourceLogo}
                                        </a>
                                    </div>
                                {/block:ContentSource}
                                </section>
                            {/block:Video}

                            <ul class="
                                post_info
                                {block:IfPlaceTimestampInLeftColumn}
                                    {block:Text} floating{/block:Text}
                                    {block:Answer} floating{/block:Answer}
                                    {block:Photo}{block:Caption} floating{/block:Caption}{/block:Photo}
                                    {block:Photo}{block:ContentSource} floating{/block:ContentSource}{/block:Photo}
                                    {block:Photoset}{block:Caption} floating{/block:Caption}{/block:Photoset}
                                    {block:Photoset}{block:ContentSource} floating{/block:ContentSource}{/block:Photoset}
                                    {block:Quote} floating{/block:Quote}
                                    {block:Link}{block:Description} floating{/block:Description}{/block:Link}
                                    {block:Link}{block:ContentSource} floating{/block:ContentSource}{/block:Link}
                                    {block:Chat} floating{/block:Chat}
                                    {block:Audio}{block:Caption} floating{/block:Caption}{/block:Audio}
                                    {block:Audio}{block:ContentSource} floating{/block:ContentSource}{/block:Audio}
                                    {block:Video}{block:Caption} floating{/block:Caption}{/block:Video}
                                    {block:Video}{block:ContentSource} floating{/block:ContentSource}{/block:Video}
                                {/block:IfPlaceTimestampInLeftColumn}
                            ">
                                {block:Date} 
                                <li>
                                    <ul class="post_controls group">
                                        <li>{ReblogButton size="21"}</li>
                                        <li>{LikeButton size="21"}</li>
                                    </ul>
                                </li>
                                {/block:Date} 
                                <li><a href="{Permalink}" class="
                                    timestamp
                                    {block:Text}has_caption{block:Title} with_title{/block:Title}{/block:Text}
                                    {block:Photo}{block:Caption}has_caption{/block:Caption}{/block:Photo}
                                    {block:Photoset}{block:Caption}has_caption{/block:Caption}{/block:Photoset}
                                    
                                    {block:Quote}
                                        {block:Source}
                                            {Length}_quote
                                        {/block:Source}
                                    {/block:Quote}
                                    
                                    {block:Link}{block:Description}has_caption{/block:Description}{/block:Link}
                                    {block:Chat}chat{block:Title} with_title{/block:Title}{/block:Chat}
                                    {block:Audio}{block:Caption}has_caption{/block:Caption}{/block:Audio}
                                    {block:Video}{block:Caption}has_caption{/block:Caption}{/block:Video}
                                ">{block:IndexPage}{TimeAgo}{/block:IndexPage}{block:PermalinkPage}{block:Date}{Month} {DayOfMonth}, {Year} ({12Hour}:{Minutes} {AmPm}){/block:Date}{/block:PermalinkPage}</a></li>{block:PermalinkPage}{block:HasTags}{/block:HasTags}{/block:PermalinkPage}

                                {block:IfShowPostNotes}
                                    {block:NoteCount}
                                       <li><a class="notecount" href="{Permalink}#notes">{NoteCount} notes</a></li>
                                   {/block:NoteCount}
                                {/block:IfShowPostNotes}

                                {block:IfShowTags}
                                    {block:Tags}
                                        <li><a class="tag" href="{TagURL}"><span>#</span>{Tag}</a></li>
                                    {/block:Tags}
                                {/block:IfShowTags}
                                </ul>
                                {block:PostNotes}
                                    <section class="post_notes">
                                        <a name="notes">
                                            {PostNotes}
                                        </a>
                                    </section>
                                {/block:PostNotes}

                                {block:IfDisqusShortname}{block:IndexPage}
                                   <section class="caption group">
                                        <a class="disquscomments" href="{Permalink}#disqus_thread">{NoteCount} Comments</a>
                                    </section>
                                {/block:IndexPage}{/block:IfDisqusShortname}
                                {block:IfDisqusShortname}{block:Permalink}
                                    <div id="disqus_thread"></div>
                                    <script type="text/javascript" src="http://disqus.com/forums/{text:Disqus Shortname}/embed.js"></script>
                                    <noscript><a href="http://{text:Disqus Shortname}.disqus.com/?url=ref">View the discussion thread.</a></noscript>
                                {/block:Permalink}{/block:IfDisqusShortname}

                                </section>
                    </li>

                {/block:Posts}
                <!-- END POSTS -->
            </ul>
            
            {block:IfDisqusShortname}
                <script type="text/javascript">
                //<![CDATA[
                (function() {
                    var links = document.getElementsByTagName('a');
                    var query = '?';
                    for(var i = 0; i < links.length; i++) {
                        if(links[i].href.indexOf('#disqus_thread') >= 0) {
                            query += 'url' + i + '=' + encodeURIComponent(links[i].href) + '&';
                        }
                    }
                    document.write('<script charset="utf-8" type="text/javascript" src="http://disqus.com/forums/{text:Disqus Shortname}/get_num_replies.js' + query + '"></' + 'script>');
                })();
                //]]>
                </script>
            {/block:IfDisqusShortname}

            <footer id="footer">
                {block:IfShowCopyrightInFooter}
                    <section class="copyright">&copy; {CopyrightYears} {Title}</section>
                {/block:IfShowCopyrightInFooter}
                {block:Pagination}
                    <nav class="pagination">
                        <section class="buttons">
                            {block:PreviousPage}<a href="{PreviousPage}" class="left">{lang:Previous page}<span class="arrow"></span></a>{/block:PreviousPage}
                            {block:NextPage}<a href="{NextPage}" class="right">{lang:Next page}<span class="arrow"></span></a>{block:NextPage}
                        </section>
                        <section class="disabled buttons">
                            <li class="left"><span class="arrow"></span></li>
                            <li class="right"><span class="arrow"></span></li>
                        </section>
                        <section class="count">Page  {CurrentPage} / {TotalPages}</section>
                    </nav>
                {/block:Pagination}
            </footer>
        </section>

        {block:IfUseEndlessScrolling}
        <script type="text/javascript" src="http://assets.tumblr.com/assets/scripts/jquery-1.7.2.min.js"></script>
        <script type="text/javascript">
            var Tumblelog = {};

            // AJAX
            Tumblelog.Ajax = (function(url, callbackFunction) {
                this.bindFunction = function (caller, object) {
                    return function() {
                        return caller.apply(object, [object]);
                    };
                };

                this.stateChange = function (object) {
                    if (this.request.readyState==4) this.callbackFunction(this.request.responseText);
                };

                this.getRequest = function() {
                    if (window.ActiveXObject)
                        return new ActiveXObject('Microsoft.XMLHTTP');
                    else if (window.XMLHttpRequest)
                        return new XMLHttpRequest();
                    return false;
                };

                this.postBody = (arguments[2] || "");
                this.callbackFunction=callbackFunction;
                this.url=url;
                this.request = this.getRequest();

                if(this.request) {
                    var req = this.request;
                    req.onreadystatechange = this.bindFunction(this.stateChange, this);

                    if (this.postBody!=="") {
                        req.open("POST", url, true);
                        req.setRequestHeader('X-Requested-With', 'XMLHttpRequest');
                        req.setRequestHeader('Content-type', 'application/x-www-form-urlencoded');
                        req.setRequestHeader('Connection', 'close');
                    } else {
                        req.open("GET", url, true);
                    }

                    req.send(this.postBody);
                }
            });
            
            // Infinite Scroll
            Tumblelog.Infinite = (function() {

                var _$window          = $(window);
                var _$posts           = $('#posts');
                var _trigger_post     = null;

                var _current_page     = {CurrentPage};
                var _total_pages      = {TotalPages};
                var _url              = document.location.href.split("#")[0];
                var _infinite_timeout = null;
                var _is_loading       = false;
                var _posts_loaded     = false;
                
                var _Ajax = Tumblelog.Ajax;

                function init() {            
                    set_trigger();
                    enable_scroll();
                }

                function set_trigger () {
                    var $all_posts = _$posts.find('li.post');
                
                    if (!_posts_loaded) {
                        _posts_loaded = $all_posts.length;
                    }

                    if (_posts_loaded >= 4) {
                        _trigger_post = _$posts.find('li.post:eq(' + ($all_posts.length - 4) + ')').get(0);
                    } else if (_posts_loaded >= 3) {
                        _trigger_post = _$posts.find('li.post:eq(' + ($all_posts.length - 3) + ')').get(0);
                    } else {
                        _trigger_post = _$posts.find('li.post:last').get(0);
                    }
                };

                function in_viewport (el) {
                    if (el == null) return;
                    var top = el.offsetTop;
                    var height = el.offsetHeight;

                    while (el.offsetParent) {
                        el = el.offsetParent;
                        top += el.offsetTop;
                    }

                    return (top < (window.pageYOffset + window.innerHeight));
                };

                function enable_scroll() {
                    $('#footer .pagination').hide();
                    _$window.scroll(function(){
                        clearTimeout(_infinite_timeout);
                        infinite_timeout = setTimeout(infinite_scroll, 100);
                    });
                }

                function disable_scroll() {
                    clearTimeout(_infinite_timeout);
                    $(window).unbind('scroll');
                }

                function infinite_scroll() {
                    if (_is_loading) return;

                    if (in_viewport(_trigger_post)) {
                        load_more_posts(); // w00t
                    }
                };

                function load_more_posts() {
                    if (_is_loading) return;
                    _is_loading = true;

                    // Build URL
                    if (_url.charAt(_url.length - 1) != '/') _url += '/';
                    if (_current_page === 1) _url += 'page/1';
                    _current_page++;
                    _url = _url.replace('page/' + (_current_page - 1), 'page/' + _current_page);

                    // Fetch
                    _Ajax(_url, function(data) {
                        var new_posts_html = data.split('<!-- START' + ' POSTS -->')[1].split('<!-- END' + ' POSTS -->')[0];
                        var $new_posts = $('#posts', data);

                        // Insert posts and update counters
                        $('#posts').append(new_posts_html);
                        _posts_loaded = $new_posts.find('li.post').length;

                        if (_posts_loaded) {
                            var post_ids = [];
                            var like_buttons = $('#posts', data).find('.like_button');
                            for (var i = 0; i < like_buttons.length; i++) {
                                var button = like_buttons[i];
                                if ($(button).attr('data-post-id')) {
                                    post_ids.push($(button).attr('data-post-id'));
                                }
                            }
                            if (post_ids.length > 0) Tumblr.LikeButton.get_status_by_post_ids(post_ids);
                        }

                        if ((_posts_loaded > 0) && (_current_page < _total_pages)) {
                            set_trigger();
                            _is_loading = false;

                        } else {
                            disable_scroll();
                        }
                    });

                    // Stats
                    {block:IfGoogleAnalyticsID}
                        if (typeof window._gaq != 'undefined') {
                            _gaq.push(['_trackPageview', _url]);
                        }
                    {/block:IfGoogleAnalyticsID}
                }

                return {
                    init: init
                };
            });

            $(function() {
                {block:IndexPage}
                if ( !($.browser.msie && (parseInt($.browser.version, 10) < 9) ) ) {
                    var InfiniteScroll = new Tumblelog.Infinite;
                    InfiniteScroll.init();
                }
                {/block:IndexPage}
            });
        </script>
        {/block:IfUseEndlessScrolling}

        {block:Twitter}
            <script type="text/javascript" src="/tweets.js"></script>
        {/block:Twitter}

        {block:IfGoogleAnalyticsID}
            <script type="text/javascript">
                var _gaq=[['_setAccount','{text:Google Analytics ID}'],['_trackPageview']];
                        (function(d,t){var g=d.createElement(t),s=d.getElementsByTagName(t)[0];
                        g.src=('https:'==location.protocol?'//ssl':'//www')+'.google-analytics.com/ga.js';
                        s.parentNode.insertBefore(g,s)}(document,'script'));
            </script>
        {/block:IfGoogleAnalyticsID}
    </body>
</html>
