MVC-Views
=========

Display / Hide an item or items on a View dependent on a condition

There are times you might want to display or hide an item on an MVC View.

A small C# code can do that as follows : (Most of the code has been taken out for the clarity)

=========================================================
@model IEnumerable<PaketYemek.Models.UrunViewModel>

@foreach (var item in Model)
{
....some code.....
 if (item.opsiyon1 != null)
        {
            <div class="row-fluid">
                <div class="span2">
                    @Html.CheckBox("opsiyon1")
                    @Html.DisplayFor(modelItem => item.opsiyon1) &nbsp;-&nbsp;
                    @Html.DisplayFor(modelItem => item.opsiyon1_fiyat) TL
                  
                </div>
            </div>
        }
       ....some code.....
}

