Split Blockquote - TinyMCE plugin
=================================

What's Split Blockquote ?
-------------------------

This plugin aims to split blockquotes when the user try to break lines in teams.
In the example bellow, the user cursor is marked with the '|' caracter:

    _________________________________________________________________________________________________
               Before LineBreak insertion            |            After LineBreak insertion
    _________________________________________________|_______________________________________________
    <body>                                           | <body>
      <blockquote>                                   |   <blockquote>
        This is a comment which has been quoted.|    |     This is a comment which has been quoted.
        Try it :-) !                                 |   </blockquote>
      </blockquote>                                  |   <p>|</p>
    </body>                                          |   <blockquote>
                                                     |     Try it :-) !
                                                     |   </blockquote>
                                                     | </body>
    _________________________________________________|_______________________________________________
    <body>                                           | <body>
      <blockquote>                                   |   <blockquote>
        <blockquote>                                 |     <blockquote>
          <blockquote>                               |       <blockquote>
            hi all, what's up ?                      |         Hi all, what's up ?
          </blockquote>                              |       </blockquote>
          <span style="color:blue;">                 |       <span style="color:blue;">
            Just try to write examples.|             |         Just try to write examples.
            And you ? What's up ?                    |       </span>
          </span>                                    |     </blockquote>
        </blockquote>                                |   </blockquote>
        I'm going to split those blockquote :p       |   <p>|</p>
      </blockquote>                                  |   <blockquote>
    </body>                                          |     <blockquote>
                                                     |       <span style="color:blue;">
                                                     |         And  you ? What's up ?
                                                     |       </span>
                                                     |     </blockquote>
                                                     |     I'm going to split those blockquote :p
                                                     |   </blockquote>
                                                     | </body>
    _________________________________________________|_______________________________________________

How to install it ?
-------------------

* Copy the tiny_mce/plugins/splitblockquote/ directory into the tinyMCE plugins directory
* Add 'splitblockquote' into the 'plugins' options, when initialize tinyMCE
  tinyMCE.init({
          ...
          plugins : 'spliblockquote,...'
  });
