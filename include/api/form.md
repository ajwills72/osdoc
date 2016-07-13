<div class="ClassDoc YAMLDoc" id="form" markdown="1">

# class __form__

The `form` is a container for widgets, such as labels, etc. If you use the
FORM_BASE plugin in combination with OpenSesame script, you do not need
to explicitly create a form. However, if you use Python inline code, you
do.

__Example__:

~~~ .python
from libopensesame import widgets
form = widgets.form(exp)
label = widgets.label(form, text='label)
form.set_widget(label, (0,0))
form._exec()
~~~

[TOC]

<div class="FunctionDoc YAMLDoc" id="form-__init__" markdown="1">

## function __form\.\_\_init\_\___\(experiment, cols=2, rows=2, spacing=10, margins=\(100, 100, 100, 100\), theme=u'gray', item=None, timeout=None, clicks=False\)

Constructor.

__Arguments:__

- `experiment` -- An OpenSesame experiment.
	- Type: experiment

__Keywords:__

- `cols` -- The number of columns (as int) or a list that specifies the number and relative size of the columns. For example, `[1,2,1]` will create 3 columns where the middle one is twice as large as the outer ones.
	- Type: int, list
	- Default: 2
- `rows` -- Analogous to `cols`, but for the rows.
	- Type: int, list
	- Default: 2
- `spacing` -- The amount of empty space between widgets (in pixels).
	- Type: int
	- Default: 10
- `margins` -- The amount of empty space around the form. This is specified as a list, like so [top-margin, right-margin, bottom-margin, left-margin].
	- Type: list
	- Default: (100, 100, 100, 100)
- `theme` -- The theme for the widgets.
	- Type: str, unicode
	- Default: 'gray'
- `item` -- The item of which the form is part.
	- Type: item, NoneType
	- Default: None
- `timeout` -- A timeout value in milliseconds, or None if no timeout exists.
	- Type: int, float, NoneType
	- Default: None
- `clicks` -- If enabled, an auditory click is played on user interactions. This can help to make interactions feel smoother if there is some visual lag.
	- Type: bool
	- Default: False

</div>

[form.__init__]: #form-__init__
[__init__]: #form-__init__

<div class="FunctionDoc YAMLDoc" id="form-_exec" markdown="1">

## function __form\.\_exec__\(focus\_widget=None\)

Executes the form.

__Keywords:__

- `focus_widget` -- A widget that is in the form and should receive a virtual mouse click when the form is opened. This allows you to activate a text_input right away, for example, so that the user doesn't have to click on it anymore.
	- Type: widget, NoneType
	- Default: None

__Returns:__

Gives the return value of the form, which depends on how the user interacted with the widgets. For example, if the user pressed a button, the button text will be returned. If a timeout occurred, None will be returned.

</div>

[form._exec]: #form-_exec
[_exec]: #form-_exec

<div class="FunctionDoc YAMLDoc" id="form-cell_index" markdown="1">

## function __form\.cell\_index__\(pos\)

Converts a position to a cell index. A cell index corresponds to the number of the cell in the form, from left-to-right, top-to-bottom.

__Arguments:__

- `pos` -- A position in the form, which can be an index (int) or a (column, row) tuple.
	- Type: int, tuple

__Returns:__

A cell index.

- Type: int

</div>

[form.cell_index]: #form-cell_index
[cell_index]: #form-cell_index

<div class="FunctionDoc YAMLDoc" id="form-render" markdown="1">

## function __form\.render__\(\)

Draws the form and all the widgets in it.

</div>

[form.render]: #form-render
[render]: #form-render

<div class="FunctionDoc YAMLDoc" id="form-set_widget" markdown="1">

## function __form\.set\_widget__\(widget, pos, colspan=1, rowspan=1\)

Adds a widget to the form.

__Arguments:__

- `widget` -- The widget to add.
	- Type: widget
- `pos` -- The position to add the widget, which can be an index or a (column, row) tuple.
	- Type: int, tuple

__Keywords:__

- `colspan` -- The number of columns that the widget should span.
	- Type: int
	- Default: 1
- `rowspan` -- The number of rows that the widget should span.
	- Type: int
	- Default: 1

</div>

[form.set_widget]: #form-set_widget
[set_widget]: #form-set_widget

<div class="FunctionDoc YAMLDoc" id="form-xy_to_index" markdown="1">

## function __form\.xy\_to\_index__\(xy\)

Converts a coordinate in pixels to a cell index. This allows you to determine on which widget a user has clicked.

__Arguments:__

- `xy` -- An (x,y) coordinates tuple.
	- Type: tuple

__Returns:__

A cell index.

- Type: int

</div>

[form.xy_to_index]: #form-xy_to_index
[xy_to_index]: #form-xy_to_index

</div>

[form]: #form
