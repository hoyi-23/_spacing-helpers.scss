# _grid.scss

//grid(欄位/欄寬 px/gutter px)

@mixin grid($columns,$col-width,$gutter) {
	.column {
		margin: 0 $gutter $gutter 0;
		float: left;
		@for $i from 1 through $columns {
			.col#{$i} {
				width: ($col-width * $i) + ($gutter * ($i - 1));
			}
		}
	}
}


// example:

.container {
	// 我想要12欄，每欄65px寬，欄與欄間隔30px距離
	@include grid(12, 65px, 30px);
}

// 會產生如下結果:

.container .column .col1 {
  width: 65px; }
.container .column .col2 {
  width: 160px; }
.container .column .col3 {
  width: 255px; }
.container .column .col4 {
  width: 350px; }
.container .column .col5 {
  width: 445px; }
.container .column .col6 {
  width: 540px; }
.container .column .col7 {
  width: 635px; }
.container .column .col8 {
  width: 730px; }
.container .column .col9 {
  width: 825px; }
.container .column .col10 {
  width: 920px; }
.container .column .col11 {
  width: 1015px; }
.container .column .col12 {
  width: 1110px; }
