<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>نموذج تسليم المركبة</title>
  <style>
    body {
      font-family: "Segoe UI", Tahoma, sans-serif;
      direction: rtl;
      text-align: center;
      margin: 40px;
      background-color: #fff;
    }

    h1 {
      color: orange;
      font-size: 20px;
    }

    table {
      width: 100%;
      border-collapse: collapse;
      margin-bottom: 20px;
    }

    th, td {
      border: 1px solid #000;
      padding: 8px;
      vertical-align: middle;
    }

    th {
      background-color: #f1f1f1;
      font-weight: bold;
    }

    input[type="text"], input[type="date"], input[type="time"] {
      width: 90%;
      padding: 6px 8px;
      font-size: 15px;
      border: 1px solid #ccc;
      border-radius: 6px;
      text-align: center;
    }

    .small-text {
      font-size: 14px;
    }

    .section-title {
      background-color: #f8f8f8;
      font-weight: bold;
      text-align: center;
      font-size: 16px;
    }

    .car-container, .fuel-container {
      position: relative;
      display: inline-block;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 8px;
      overflow: hidden;
    }

    .car-container img, .fuel-container img {
      width: 250px;
      height: auto;
      display: block;
    }

    .marker {
      position: absolute;
      width: 16px;
      height: 16px;
      border-radius: 50%;
      background-color: rgba(255, 0, 0, 0.7);
      transform: translate(-50%, -50%);
      cursor: pointer;
      border: 1px solid #a00;
    }

    .fuel {
      width: 240px;
    }

    .signature {
      color: orange;
      font-weight: bold;
    }

    .name {
      color: #0040ff;
      font-weight: bold;
    }

    .time {
      color: #0040ff;
    }

    .note {
      text-align: center;
      color: #555;
      font-size: 14px;
      margin-top: 5px;
    }

    .datetime-cell {
      display: flex;
      justify-content: space-around;
      align-items: center;
      gap: 5px;
    }

    .datetime-cell input[type="date"],
    .datetime-cell input[type="time"] {
      width: 45%;
    }
  </style>
</head>
<body>

  <h1>رقم تسلسلي /</h1>

  <!-- جدول رقم اللوحة ونوع السيارة -->
  <table>
    <tr>
      <th style="width: 25%;">نوع السيارة</th>
      <td style="width: 25%;"><input type="text" placeholder="مثال: باجيرو"></td>
      <th style="width: 25%;">رقم اللوحة</th>
      <td style="width: 25%;"><input type="text" placeholder="مثال: أ ب ج 1234"></td>
    </tr>
  </table>

  <!-- جدول الحالة قبل وبعد الاستخدام -->
  <table>
    <tr>
      <th class="section-title">حالة السيارة قبل الاستخدام</th>
      <th class="section-title">حالة السيارة بعد الاستخدام</th>
    </tr>
    <tr>
      <td>
        قراءة العداد:
        <input type="text" placeholder="مثال: 12500 كم">
      </td>
      <td>
        قراءة العداد:
        <input type="text" placeholder="مثال: 12800 كم">
      </td>
    </tr>
    <tr>
      <td>
        <div class="car-container" id="carBefore">
          <img src="car.png.png" alt="صورة السيارة قبل الاستخدام">
        </div>
        <div class="note">انقر لتحديد الأضرار (انقر على العلامة لإزالتها)</div>
      </td>
      <td>
        <div class="car-container" id="carAfter">
          <img src="car.png.png" alt="صورة السيارة بعد الاستخدام">
        </div>
        <div class="note">انقر لتحديد الأضرار (انقر على العلامة لإزالتها)</div>
      </td>
    </tr>
   
    <tr>
      <td>
        <div class="fuel-container" id="fuelBefore">
          <img src="car bt.png" alt="عداد البنزين" class="fuel">
        </div>
        <div class="note">انقر لتحديد مستوى البنزين</div>
      </td>
      <td>
        <div class="fuel-container" id="fuelAfter">
          <img src="car bt.png" alt="عداد البنزين" class="fuel">
        </div>
        <div class="note">انقر لتحديد مستوى البنزين</div>
      </td>
    </tr>
    <tr>
      <td>اسم المستلم: <input type="text" placeholder="اكتب اسم المستلم هنا"></td>
       <td>اسم المستلم: <span class="name">جمال محمد عبده حكمي</span></td></tr>
    <tr>
      <td>
        <div class="datetime-cell">
          <label>تاريخ الاستلام:</label>
          <input type="date">
          <input type="time">
        </div>
      </td>
      <td>
        <div class="datetime-cell">
          <label>تاريخ التسليم:</label>
          <input type="date">
          <input type="time">
        </div>
      </td>
    </tr>
    <tr>
      <td><span class="signature1">التوقيع:</span></td>
      <td><span class="signature2">التوقيع:</span></td>
    </tr>
  </table>
  <h2 class="declaration-title">إقرار وتفويض قيادة المركبة والمهام</h2>

  <table>
    <tr>
      <th>إقرار استلام</th>
    </tr>
    <tr>
      <td>
        <div class="declaration-box">
          أقر أنا الموقع أدناه بأنني استلمت المركبة الموصوفة أعلاه لاستخدامها في أداء المهمة الرسمية المحددة من قبل الجهة، وأتعهد بالحفاظ عليها واستعمالها بما يخالف القوانين والتعليمات الداخلية. كما أقر بتحمل المسؤولية عن أي أضرار أو مخالفات تنتج عن سوء الاستخدام.
        </div>
      </td>
    </tr>
  

  
    <tr>
      <th>تفويض المركبة</th>
    </tr>
    <tr>
      <td>
        <div class="declaration-box">
          بموجب هذا أُفوِّض السيد/السيدة المذكور(ة) أدناه بقيادة المركبة لأداء المهام الموكولة إليه(إليها) من قبل الجهة خلال الفترة المحددة، ويشمل التفويض صلاحية استخدام المركبة للمهام الرسمية فقط. ويعتبر هذا التفويض نافذاً من تاريخ التوقيع أعلاه وحتى الانتهاء من المهمة أو سحبه خطياً.
        </div>
      </td>
    </tr>
    <tr>
      <th>المهام أو الزيارات </th>
    </tr>
     <tr>
      <td>
        <div class="declaration-box">
          جولات ميدانيه او مراجعة الامانه او جدزر فرسان او استقبال الوفد وغيرها 
        </div>
      </td>
    </tr>
  </table>
<table>
  <tr>
    <th class="section-title" colspan="2">التوقيع عند الاستلام</th>
    <th class="section-title" colspan="2">التوقيع عند التسليم</th>
  </tr>
  <tr>
    <th>اسم المستلم</th>
    <th>التوقيع</th>
    <th>اسم المستلم</th>
    <th>التوقيع</th>
  </tr>
  <tr>
    <td><input type="text" placeholder="اكتب الاسم هنا"></td>
    <td><input type="text" placeholder="التوقيع"></td>
    <td><span class="name">جمال محمد عبده حكمي</span></td>
    <td></td>
  </tr>
  <tr>
    <th>صاحب الصلاحية</th>
    <th>التوقيع</th>
    <th>صاحب الصلاحية</th>
    <th>التوقيع</th>
  </tr>
  <tr>
    <td><span class="name">جمال محمد عبده حكمي</span></td>
    <td></td>
    <td><span class="name">جمال محمد عبده حكمي</span></td>
    <td></td>
  </tr>
</table>
<!-- تعهد استخدام -->
<h2 style="color: orange; text-align: center; margin-top: 30px;">تعهد استخدام</h2>

<div style="text-align: right; line-height: 1.9; font-size: 15px; margin: 0 40px;">
  <p>يتعهد المستخدم لما يلي بشأن استخدام سيارة الجهة:</p>
  <ol style="padding-right: 25px;">
    <li>لا يسمح بقيادة السيارات لأي شخص لا يحمل رخصة قيادة سارية المفعول أو دون سن <strong>(21)</strong> سنة، ويشترط أن يكون سائق السيارات أحد منسوبي الإدارة ذات العلاقة.</li>
    <li>تخصيص السيارة فقط للأعمال الرسمية وفق المهمة وقت العمل أو المهام والإجراءات المعتمدة، وإيقاف السيارة في مقر الإدارة أو الموقع بعد انتهاء المهمة وتسليم المفاتيح للمسؤول عن المركبات.</li>
    <li>عدم استخدام السيارة في الأغراض الشخصية أو خارج أوقات العمل الرسمية أو نقل الركاب أو الأثاث أو الأغراض الشخصية أو في شكل استئجار أو تسليمها لشخص آخر.</li>
    <li>الالتزام بالسعة النظامية للمركبة وعدم تحميلها أكثر من المسموح به، واستخدامها في الطرق المعبدة فقط، وعدم استخدام المركبة في السحب أو جر السيارات، وألا تتجاوز السرعة المحددة وهي <strong>(120 كم/س)</strong>.</li>
    <li>عدم التدخين داخل السيارة أو إلقاء المخلفات داخلها أو خارجها أثناء القيادة، والمحافظة على نظافة السيارة من الداخل والخارج، والإبلاغ فورًا عند وجود أي خلل أو عطل فني.</li>
    <li>في حالة وقوع حادث أو عطل فني يلزم إبلاغ الجهة المختصة فورًا وعدم ترك الموقع إلا بعد اتخاذ الإجراءات اللازمة مع الجهات الأمنية والتأمين.</li>
    <li>يتحمل المستخدم مسؤولية أي مخالفات مرورية أو تلفيات أو فقدان لأي من محتويات السيارة أثناء فترة استخدامها.</li>
    <li>عدم إجراء أي تعديلات على السيارة أو تركيب إضافات دون إذن مسبق من الإدارة المختصة.</li>
    <li>عدم استخدام السيارة خارج حدود المنطقة إلا بتصريح رسمي من الجهة المختصة.</li>
    <li>أقر بالاطلاع والتقيد بكافة الشروط الواردة في هذا التعهد وبنوده، والله على ما أقول شهيد.</li>
  </ol>
</div>

<!-- جدول بيانات السيارة وملاحظة التواصل -->
<table>
  <tr style="background-color: #f1f1f1; font-weight: bold; text-align: center;">
    <th>نوع السيارة</th>
    <th>اللوحة</th>
    <th>الموديل</th>
    <th>اللون</th>
    <th>الحالة</th>
  </tr>
  <tr style="text-align: center;">
    <td><input type="text" placeholder="اكتب نوع السيارة" style="width: 95%; text-align: center;"></td>
    <td><input type="text" placeholder="اكتب رقم اللوحة" style="width: 95%; text-align: center;"></td>
    <td><input type="text" placeholder="اكتب الموديل" style="width: 95%; text-align: center;"></td>
    <td><input type="text" placeholder="اكتب اللون" style="width: 95%; text-align: center;"></td>
    <td>جديدة من الوكالة</td>
  </tr>
</table>

<p style="text-align: right; font-size: 15px; margin-top: 5px;">
  للاستفسار يرجى التواصل مع مسؤول النقل في مقر الإدارة جوال رقم 
  
  
  <a href="tel:0545105222" style="color: blue; text-decoration: none;">(0545105222)</a>
<tr></tr>
</p>
<p style="text-align: right; font-size: 15px; margin-top: 5px;">
الجهة : هيئة التراث بجازان 

  <a href= style="color: blue; text-decoration: none;"></a>
<tr></tr>
</p>

    
 
  </tr>
</table>

  <script>
    function enableImageMarking(containerId) {
      const container = document.getElementById(containerId);

      container.addEventListener('click', function(event) {
        const rect = container.getBoundingClientRect();
        const x = event.clientX - rect.left;
        const y = event.clientY - rect.top;

        const marker = document.createElement('div');
        marker.classList.add('marker');
        marker.style.left = `${x}px`;
        marker.style.top = `${y}px`;

        marker.addEventListener('click', e => {
          e.stopPropagation();
          marker.remove();
        });

        if (container.classList.contains('fuel-container')) {
          const oldMarker = container.querySelector('.marker');
          if (oldMarker) oldMarker.remove();
        }

        container.appendChild(marker);
      });
    }

    enableImageMarking('carBefore');
    enableImageMarking('carAfter');
    enableImageMarking('fuelBefore');
    enableImageMarking('fuelAfter');
  </script>

</body>
</html>
