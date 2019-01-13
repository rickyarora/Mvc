
Thanks

@model MachTest.Models.vmEmployee
@{
    ViewBag.Title = "Create";
}

<h2>Create</h2>
@using (Html.BeginForm("Create", "Employee", FormMethod.Post, new { enctype = "multipart/form-data" }))
{
@Html.HiddenFor(x => x.Id)
<div class="col-md-12">
    <div class="col-md-6">
        <div class="col-md-6">
            @Html.LabelFor(x => x.Name)
        </div>
        <div class="col-md-6">
            @Html.TextBoxFor(x => x.Name)
        </div>
    </div>
    <div class="col-md-6">
        <div class="col-md-6">
            @Html.LabelFor(x => x.Descrition)
        </div>
        <div class="col-md-6">
            @Html.TextBoxFor(x => x.Descrition)
        </div>
    </div>

    <div class="col-md-6">
        <label for="file">Upload Image:</label>
        <input type="file" name="file" id="file" style="width: 100%;" />
    </div>

    <div class="col-md-6"><br /></div>

    <div class="col-md-6">
        <input type="submit" value="Submit" class="btn btn-success" />
    </div>
</div>

}

