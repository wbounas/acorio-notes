# ServiceNow Fundamentals - Jakarta
## Module 01: User Interface and Navigation
## Section 1.2: Table Lists

![1.2 Table Lists Overview](https://cl.ly/2r361M2y1d1e/Image%202018-06-06%20at%206.17.59%20PM.png)



## What is a List?
A **list** displays a `set of records` from a _table_

![What is a list?](https://cl.ly/3S2J292T210t/Image%202018-06-06%20at%206.20.09%20PM.png)


`Lists` and `forms` are the most common ways to interact with `data`
- A `list` displays a _set of records_ from a `table`
- You can `filter` and `customize` **lists** to display the _information you need_


**NOTE:** you may encounter **2 different versions** of `list functionality` referred
        to `List v2` and `List v3`


## List: _Anatomy_

![List Anatomy](https://cl.ly/2i0n0m0B2R2r/Image%202018-06-07%20at%2012.29.11%20PM.png)

**List Anatomy**
1. **Title Bar:** displays `list title`, some cases `specific list view`
2. **List Filters/Breadcrumbs:** quick form of `filter navigation`
3. **Column Headings:** displays column (_field_) names, provides some `list controls`
4. **Column Header Search:** provides a `search` within a _specific column_
5. **Fields:** displays data; `right-click` to access _more actions_


Although `lists` display data captured in `different tables`, their **interface**
remains _consistent_ with `common features`



## List: _Views_

![List: Views](https://cl.ly/2m1t0f2F0a1F/Image%202018-06-07%20at%2012.28.34%20PM.png)

A **view** is a version of a `customized list or form` which defines the _layout order_
and what `fields` appear on the `list` or `form`
- For `list views`, the same # of records for that `particular table display`,
  different `fields` may be visible and _display in a different order_

**Views** enable users to _quickly display_ the same `list` or `form` in **multiple ways**
- `Sys Admins` can create **views** for `lists` or `forms`
- **EXAMPLE:** you can create and use _different views_ in `Incident` for an `ESS user`,
  an `ITIL user`, and a `mobile user`

To switch between different `views` of `columns` on a `list` (as shown here),
open the `List Context Menu` and then select **View**
- Then, select the name of the _desired view_!

The _view name_ appears in **brackets** beside the `table list title` and
`form record type` when a `view` other than the `Default view` is selected

**NOTE:** switching `views` on a form will attempt to save `all changes`
made to the record
- You'll _receive a message_ if you want to `save` or `discard` all changes
  made to the record, before the `form reloads` and `displays` the selected view

**Sort Controls:** a `list` that is displayed to a user for the _first time_
will be sorted by one of the following:
- The **order** field (if `one is present` in the table)
- The **number** field (if `one is present` in the table)
- The **name** field (if `one is present` in the table)
- The field specified as the _display field_ for the `table`

## List: _Context Menus_

![List: Context Menus](https://cl.ly/2H1J1y280n12/Image%202018-06-07%20at%2012.20.00%20PM.png)

**Context menus** (aka `Additional Actions` or `control menus`) provide different levels of
_controls_ for a `given list`
- Can be accessed by clicking the `list menu icon` or by `right-clicking` the `list header`
  and `column headers` respectively, and only for the **Record Context Menu** (`right-clicking`
  in a row's cell)

**List Context (or control) menus**, also sometimes called `Additional Actions`, can be
accessed from `lists`, `columns`, or on `records` by using `right-click menus` which provide
different **levels of controls:**
- **List Context Menu:** you can _click_ the `list context menu icon` next to the title of the
<<<<<<< HEAD
                         list to _access options_ related to viewing and filtering the entire
                         __record list__
- **Column Context Menu:** click the `column context menu icon` in the _desired column header_
                           to `display actions` _related_ to that column, such as:
                           - Creating `quick reports`
                           - Configuring the `list`
                           - Exporting `data`
- **Record Context Menu:** you can `right-click` into a _row's cell_ to see a `menu` with
                           actions related to the `values` in that `cell`, such as:
                           - Filtering Options
                           - Assigning Tags
                           - More



**List: Layout Configuration**
Configuring a list allows you to _show or hide fields_ from a `view`, as well as
change the `list column order`
- Click the `column context menu` icon and select **Configure > List Layout**


If you have the `admin` or `personalize_list` role, you can add or remove `columns` (fields)
from a `list` or _change the order_ in which columns appear in the list, for _all users_

- To do so, navigate to the list, then open the **column context menu**, then
  select **Configure**, and then select **List Layout**

The `slushbucket` opens and has two sections:
1. The **available** items on the left
2. The **select items** on the right
- Items from the available section can be added to the list and items from the
  _selected section_ can be removed from the list

- Once the items are in the `selected section`, there are controls to adjust their
  (up or down) on the list


**List Personalization**
`Personalizing a list` allows you to show or hide fields on a view, as well as _change the
list column order_

**NOTE:** Unlike `configuring` a list, `personalizing` a list **will NOT** affect
what others see on their lists
- To personalize a list view, click the `Personalize List` icon (or gear)
  from the `list column header`
- List layout changes using `List Layout` will affect everyone,
  across the entire instance (**except** for individuals
  using `personalized layouts` set via `Personalize List`)



**List Editing**
The `List Editor` allows you to edit field values in a list without
opening the form
1. Double-click in an `empty area` of the field
2. Enter the appropriate value(s)
3. Save the record by clicking the save (√)
  - **NOTE:** click the `cancel` (X) icon or pressing the `Escape Key`
    retains the original value



**Finding Information: ServiceNow Search**
Use any of the following searches to find information in `ServiceNow`
- **Lists:** find records, search in a specific field, all fields, or in
         a specific column
- **Global Text Search:** find records in multiple tables from a single
                          search field
- **Knowledge Base:** find `knowledge articles`
- **Service Catalog:** find `catalog items`
- **Filter Navigator:** filter the itesm in the `application navigator`

You can find information _quickly_ in ServiceNow by using any of the available searches:
- `Wildcards: using` a symbol to represent zero or more characters
- `Phrase Searches:` find a phrase with multiple terms
- `Searching Lists:` control the query for list searches of a specific field
- `Boolean Operators:` refine searches with operators such as AND and OR
- `Attachment Searches:` search in files that are attached to Knowledge Article recrods
- `International Character Sets:` perform seraches with any Unicode characters
- `Punctuation:` perform searches that contain punctuation


**NOTE:** Searches are not _case sensitive_
- Use advanced options for more specific queries



=======
                         list
>>>>>>> origin/master
