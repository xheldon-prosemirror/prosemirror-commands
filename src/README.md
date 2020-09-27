This module exports a number of _commands_, which are building block
functions that encapsulate an editing action. A command function takes
an editor state, _optionally_ a `dispatch` function that it can use
to dispatch a transaction and _optionally_ an `EditorView` instance.
It should return a boolean that indicates whether it could perform any
action. When no `dispatch` callback is passed, the command should do a 
'dry run', determining whether it is applicable, but not actually doing
anything.

@cn 本模块导出了一些 _命令_，它可以构建块级函数以封装一个编辑行为。一个命令函数接受一个编辑器的 state，
一个 _可选的_ `dispatch` 函数，用来 dispatch 一个 transaction，及一个 _可选的_ `EditorView`
实例作为参数。它应该返回一个布尔值以指示它是否可以执行任何行为。当没有 `dispatch` 回调被传入的时候，
该命令应该做一个 `空运行`，以决定它是否应该被运行，而不实际做任何事情。

These are mostly used to bind keys and define menu items.

@cn 这些命令大多数用来绑定按键以及定义菜单项。

@chainCommands
@deleteSelection
@joinBackward
@selectNodeBackward
@joinForward
@selectNodeForward
@joinUp
@joinDown
@lift
@newlineInCode
@exitCode
@createParagraphNear
@liftEmptyBlock
@splitBlock
@splitBlockKeepMarks
@selectParentNode
@selectAll
@wrapIn
@setBlockType
@toggleMark
@autoJoin
@baseKeymap
@pcBaseKeymap
@macBaseKeymap
