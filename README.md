# learnings.plan
1 You can add `-watch` as an arg when running/testing a Lime based project (openfl, haxeflixel, etc.), and it will auto-recompile anytime there's a file change in any of your source directories.
2 Snippet for pixel perfect HTML5 rendering for HaxeFlixel.
    ```hx
    #if web
        // pixel perfect render fix!
        Application.current.window.element.style.setProperty("image-rendering", "pixelated");
    #end
    ```
