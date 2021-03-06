---
title: Backend File Structures in Angular
localeTitle: هياكل ملف الخلفية في Angular
---
تقع واجهة المستخدم الخلفية للتطبيق التي تتفاعل مع قاعدة البيانات في **/ server / api**  
دعونا نلقي نظرة على **/ server / api / thing** :

1.  **index.js** : يوجه هذا الملف طلبات واجهة برمجة تطبيقات $ http التي يتم إجراؤها من الواجهة الأمامية للتطبيق إلى الوظيفة المناسبة في **thing.controller.js**
2.  **thing.controller.js** : هنا حيث نتعامل بالفعل مع قاعدة البيانات! خذ دقيقة للنظر من هنا ومعرفة ما يجري. ستقوم هذه الوظائف بإرجاع جميع العناصر في مجموعة ، أو إرجاع عنصر واحد من مجموعة عند تمرير معرفها ، أو نشر عنصر إلى مجموعة ، أو تحديث عنصر في المجموعة (وهذا لا يعمل على النحو المنشود من المربع ، سنقوم بإصلاح ذلك في دقيقة واحدة) ، وبالطبع ، حذف عنصر من المجموعة.
3.  **thing.model.js** : هنا ، يتم تعريف البنية الفعلية لكائن _الشيء_ . يمكنك إضافة أو إزالة أي حقول تريدها من نموذج _الشيء_ ، وطالما أنها صحيحة من الناحية التركيبية فإنها لن تكسر أي شيء ، حتى إذا كانت هناك _أشياء_ ذات مخططات مختلفة في قاعدة بياناتك بالفعل. لكن! ليس عليك فقط تعديل نموذج _الشيء_ لعمل نوع جديد من المجموعة ، لأن المولد-الزاوي-fullstack يمكنه القيام بذلك نيابة عنك!