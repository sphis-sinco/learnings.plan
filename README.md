# learnings.plan
1. You can add `-watch` as an arg when running/testing a Lime based project (openfl, haxeflixel, etc.), and it will auto-recompile anytime there's a file change in any of your source directories.
2. Snippet for pixel perfect HTML5 rendering for HaxeFlixel.
    ```hx
    #if web
        // pixel perfect render fix!
        Application.current.window.element.style.setProperty("image-rendering", "pixelated");
    #end
    ```
3. You can use
   ```hx
   @:depricated()
   ```
    for functions no longer in use and put some text in the ()'s to tell yourself its depricated

4. You can use
   ```hx
   @:haxe.warning("WDeprecated")
   ```
   to disable deprication warnings or in the terminal use the compiler conditional `-w WDeprecated`
   
