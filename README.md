# jQuery Textmeter
#### by [Planet Telex][1]

![4]
A jQuery plugin to count down the remaining text in a text area.
#### [View Demos and Complete Documentation][2]

#### Requirements:
* jQuery 1.6+

#### Features:

* Regex expression matches can be a constant length to account for URL shortening.
* Customizable "Characters left" label.
* Label can "pulse" on and off when the maximum characters has been exceeded.
* Use any CSS styling you wish.


#### Quick Start:


##### Step 1

Include jQuery and jQuery Textmeter:

	<script type="text/javascript" src="js/jquery-1.11.2.min.js"></script>
	<script type="text/javascript" src="js/jquery-textmeter.min.js"></script>

##### Step 2

Have a textarea in your HTML:

	<div id="content">
        <p>
            Begin typing into the box below to see jQuery Textmeter in action.
        </p>
        <textarea rows="10" cols="10"></textarea>
    </div>

##### Step 3

Add the JavaScript to textmeter your container:

    <script type="text/javascript">
        var pt = {};
        pt.config = {
            shortener: {
                urlLength: 10
            },
            regex: {
                "url": /\b(https?:\/\/?\w{2,}[^\s()<>]+(?:\([\w\d]+\)|([^[:punct:]\s]|\/?)))/
            }
        };
        $(function () {
            // This configuration accounts for all URLs being shortened to 20 characters.
            $("textarea").textmeter(100, {
                ignoreRegex: pt.config.regex.url,
                ignoreRepacementSize: pt.config.shortener.urlLength
            });
        });
    </script>

[See the demo in action][3] for a complete example.

#### License

##### Major Components:

* jQuery: MIT/GPL license

##### Everything Else:

    Copyright 2015 Planet Telex, Inc.

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

[1]: http://www.planettelex.com
[2]: http://www.planettelex.com/products/jquery-textmeter/demo
[3]: http://planettelex.github.io/jquery-textmeter
[4]: http://planettelex.github.io/jquery-textmeter/images/demo.png
