## Q & A

Berikut beberapa pertanyaan yang sempat tidak terjawab di acara dan sempat kami jawab 😬

---

> Bagaimana cara mengeveluate app kita secara detail seperti size (ex: drawable size, kotlin size) per module dan di visualisasikan ke dalam dashboard?

Mungkin versi simplenya bisa pake feature bawaan android studio Menu Build -> Analyze APK.

> menurut mas Hartviq, jetpack compose itu bisa ningkatin performance rendering? Based on my finding xml vs jetpack compose, masih better xml scr performance

Diakhir slide terakhir saya sedikit membahas performa jetpack compose juga, so overall setuju secara performance masih better xml dari article comparasi yang saya temukan. tapi dengan catatan gap nya gak significantly selisih kurang lebih 10% nan lah.. harapannya compose kedepannya akan ada improvement dari sisi performa juga.. amin

> Menurut mas Hartviq, mending pakai include atau viewstub secara overall?

tergantung complexity dari reusable layoutnya, kalo gw sendiri lebih prefer viewstub untuk layout yang kompleks. kalo simple layout pake include tag cukup.

> Kenapa overdraw bisa buat app jadi laggy? bukannya setiap draw itu punya thread rendering yang berbeda?

kalo yang gw pahami mas, RenderThread depends on UIThread mas, simplenya UIThread melakukan preparing/processing and commanding Render Thread untuk melakukan drawing frame. jadi kalo processing di UIThread lama akan ngefek ke renderTread juga. CMIIW

> Tools untuk mendeteksi memory leak lebih baik pakai leak canary atau profiler bawaan android studio mas?

leak canary mas, karena cukup di embed ke apk testing kita, kalo profiler agak effort karena kita harus melakukan manual debugging.

> Untuk profiling yg lebih baik, apakah direkomendasikan untuk update ke chipmunk?

yup gw rekomendasikan, apalagi kalo pengen detect jank frames di android 12 or higher..
