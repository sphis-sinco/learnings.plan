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
   
5. You can use
   ```hx
   haxe.PosInfos
   ```
   for things related to position in code, for example
   ```hx
   class Main {
      static function assert(cond:Bool, ?pos:haxe.PosInfos) {
        if (!cond)
          haxe.Log.trace("Assert in " + pos.className + "::" + pos.methodName, pos);
      }

      static function main() {
        assert(1 == 1); // nothing
        assert(0 == 3); // trace "Assert in Test::main"
      }
    }
   ```
   
6. Dynamic Functions can be overriden by just doing this
    ```hx
    updateScore = function(miss:Bool = false) { ... }
    ```

7. For defines `-D value=any` means it ends up `any=any` and
```hx
// looking for it being a bumber
#if (value > 5)
```
will result in an error.
