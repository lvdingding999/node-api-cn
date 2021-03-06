<!-- YAML
added: v0.1.21
changes:
  - version: v13.11.0
    pr-url: https://github.com/nodejs/node/pull/31530
    description: In `recursive` mode, the first created path is returned now.
  - version: v10.12.0
    pr-url: https://github.com/nodejs/node/pull/21875
    description: The second argument can now be an `options` object with
                 `recursive` and `mode` properties.
  - version: v7.6.0
    pr-url: https://github.com/nodejs/node/pull/10739
    description: 参数 `path` 可以是 WHATWG `URL` 对象（使用 `file:` 协议）。 
      该支持目前仍是实验的。
-->

* `path` {string|Buffer|URL}
* `options` {Object|integer}
  * `recursive` {boolean} **默认值:** `false`。
  * `mode` {string|integer} Windows 上不支持。**默认值:** `0o777`。
* 返回: {string|undefined}

同步地创建目录。
返回 `undefined`，或者如果 `recursive` 为 `true`，则返回创建的第一个文件夹的路径。
[`fs.mkdir()`] 的同步版本。

也可参见 mkdir(2)。

