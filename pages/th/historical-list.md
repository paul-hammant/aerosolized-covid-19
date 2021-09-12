---
title: ประวัติของโรคติดต่อที่เกิดจากละอองลอย
permalink: /th/historical-list
layout: page
---

<script
  src="https://code.jquery.com/jquery-3.6.0.min.js"
  integrity="sha256-/xUj+3OJU5yExlq6GSYGSHk7tPXikynS7ogEvDej/m4="
  crossorigin="anonymous"></script>
<script type="text/javascript" src="https://cdn.datatables.net/1.10.11/js/jquery.dataTables.min.js"></script>
<script type="text/javascript" src="https://cdn.datatables.net/fixedcolumns/3.2.1/js/dataTables.fixedColumns.min.js"></script>
<script src="https://unpkg.com/dayjs@1.8.21/dayjs.min.js"></script>
<link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/1.10.25/css/jquery.dataTables.min.css">


มีการพูดคุยกันถึงลักษณะของการติดเชื้อในอากาศหรือละอองลอยสำหรับโรคอื่น ๆ ในช่วงหลายปีที่ผ่านมา ซึ่งประกอบด้วยการพัฒนาที่สำคัญ ๆ ในหลายประการในหัวข้อเหล่านี้ <a href="https://twitter.com/intent/tweet?url=https%3A%2F%2Fits-airborne.org%2Fhistorical-list&via=AerosolizedC19&text=%23COVIDisAirborne%20%23masks4All%20%23bewareOfSharedAir%20%23ventilation. See: " target="_blank">ทวีตหน้านี้</a>

โดยในไทม์ไลน์นี้ ละอองลอย = ในอากาศ = ละอองฝอยขนาดเล็ก อนุภาคเหล่านี้เป็นอนุภาคที่มีเส้นผ่านศูนย์กลางน้อยกว่า 100 ไมโครเมตร ปกติแล้วจะระเหยไปก่อนที่แรงโน้มถ่วงจะดึงพวกมันลงสู่พื้น เนื่องจากเป็นอนุภาคขนาดเล็ก พวกมันจะลอยเป็นเวลาหลายนาทีหรือเป็นชั่วโมง และสามารถเดินทางไปได้ไกลในช่วงเวลาดังกล่าว
คำว่าละอองลอยหมายถึงอนุภาคที่ลอยอยู่ในอากาศ

ในทางกลับกัน *ละอองฝอยขนาดใหญ่* ซึ่งเป็นอนุภาคที่มีเส้นผ่านศูนย์กลางใหญ่กว่า 100 ไมโครเมตร มักจะถูกแรงโน้มถ่วงดึงให้ตกลงมาที่พื้น ซึ่งกล่าวกันว่าจะเกิดขึ้นภายในระยะสองเมตร และปกติจะเกิดก่อนที่พวกมันจะระเหยและลอยตัว


หมายเหตุ ชุมชนทางการแพทย์และวิทยาศาสตร์กำลังเปลี่ยนคำจำกัดความของละอองฝอยขนาดใหญ่ให้เป็นอนุภาคขนาด 100 ไมโครเมตรขึ้นไป ซึ่งเดิมคือ 5 ไมโครเมตร <a target="_blank" href="https://twitter.com/linseymarr/status/1336318245348003840">ดูทวีตของ @linseymarr</a>. ทุกอย่างที่มีขนาดเล็กกว่า 100 μm ถือเป็นละอองลอย ดูเพิ่มเติมที่ไทม์ไลน์ (historical-timeline.html) ของหน้านี้

<script>
$(document).ready(function () {
    $.noConflict();

       $.getJSON("../media/aerosol-history-timeline.json", function(tl) {
            for(i=0;i < tl.events.length;i++){
                    var html='';
                    var dt = tl.events[i].start_date.year; 
                    var mt = tl.events[i].start_date.month;
                    var dy = tl.events[i].start_date.day;
                    if (mt > 0) {
                        dt = dt + "-" + mt;     
                        if (dy > 0) {
                            dt = dayjs(dt + "-" + dy).format('MMM D, YYYY');     
                        } else {
                            dt = dayjs(dt + "-1").format('MMM, YYYY');    
                        }
                    }

                    dt = dt.replaceAll("-undefined","");
                    html +='<td>' + dt +'</td>';
                    html +='<td><a href="' + tl.events[i].media.link +'">link</a></td>';
                    html +='<td>' + tl.events[i].text.headline +'</td>';
                    html +='<td>' + tl.events[i].text.text +'</td>';
                    $('#table_id tbody').append('<tr>'+html+'</tr>');
            }
            $('#table_id').DataTable();
       });
});
</script>

<table id="table_id" class="display">
    <thead>
        <tr>
          <th>วันที่</th>
          <th>ลิงค์</th> 
          <th>หัวข้อข่าว</th> 
          <th>เนื้อหา</th>
        </tr>
    </thead>
    <tbody>        
    </tbody>
</table>
