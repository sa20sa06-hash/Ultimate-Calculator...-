package com.aalem.riyadiyat

import android.net.Uri
import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.activity.compose.rememberLauncherForActivityResult
import androidx.activity.result.contract.ActivityResultContracts
import androidx.compose.foundation.Canvas
import androidx.compose.foundation.background
import androidx.compose.foundation.border
import androidx.compose.foundation.clickable
import androidx.compose.foundation.layout.*
import androidx.compose.foundation.lazy.LazyColumn
import androidx.compose.foundation.lazy.items
import androidx.compose.foundation.shape.RoundedCornerShape
import androidx.compose.foundation.text.BasicTextField
import androidx.compose.material3.*
import androidx.compose.runtime.*
import androidx.compose.ui.Alignment
import androidx.compose.ui.Modifier
import androidx.compose.ui.geometry.Offset
import androidx.compose.ui.graphics.Color
import androidx.compose.ui.graphics.StrokeCap
import androidx.compose.ui.text.font.FontWeight
import androidx.compose.ui.unit.dp
import androidx.compose.ui.unit.sp
import androidx.compose.ui.platform.LocalContext
import org.mariuszgromada.math.mxparser.Expression
import java.io.File
import java.io.FileOutputStream
import kotlin.math.*

private val Background = Color(0xFF05070D)
private val Panel = Color(0xFF101827)
private val Neon = Color(0xFF25E6D2)
private val Purple = Color(0xFFB18CFF)
private val White = Color(0xFFF4F7FB)
private val Muted = Color(0xFF9AA8BA)

class MainActivity : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)

        window.statusBarColor = android.graphics.Color.rgb(5, 7, 13)
        window.navigationBarColor = android.graphics.Color.rgb(5, 7, 13)

        setContent {
            MaterialTheme(
                colorScheme = darkColorScheme(
                    background = Background,
                    surface = Panel,
                    primary = Neon,
                    secondary = Purple,
                    onBackground = White,
                    onSurface = White
                )
            ) {
                MathWorldApp()
            }
        }
    }
}

private enum class AppSection(val title: String, val icon: String) {
    HOME("الرئيسية", "⌂"),
    ENCYCLOPEDIA("الموسوعة", "▤"),
    TEACHER("المعلم الذكي", "✦"),
    CALCULATOR("الحاسبة", "∑"),
    GRAPHS("الرسوم البيانية", "⌁"),
    QUIZ("الاختبارات", "✓"),
    NOTEBOOK("دفتر الرياضيات", "▧"),
    GEOMETRY("الهندسة", "△"),
    PROGRESS("التقدم", "◷"),
    SETTINGS("الإعدادات", "⚙")
}

private data class LessonCategory(
    val level: String,
    val topics: List<String>
)

@Composable
private fun MathWorldApp() {

    var selected by remember {
        mutableStateOf(AppSection.HOME)
    }

    var showMenu by remember {
        mutableStateOf(false)
    }

    Column(
        Modifier
            .fillMaxSize()
            .background(Background)
    ) {

        Header(
            onMenu = {
                showMenu = !showMenu
            }
        )

        if (showMenu) {

            LazyColumn(
                Modifier
                    .fillMaxWidth()
                    .heightIn(max = 260.dp)
                    .background(Panel)
                    .padding(8.dp)
            ) {

                items(AppSection.values().toList()) { item ->

                    Text(
                        "${item.icon}   ${item.title}",
                        color = if (selected == item) Neon else White,
                        modifier = Modifier
                            .fillMaxWidth()
                            .clickable {
                                selected = item
                                showMenu = false
                            }
                            .padding(12.dp)
                    )
                }
            }
        }

        Box(
            Modifier
                .weight(1f)
                .fillMaxWidth()
        ) {

            when (selected) {

                AppSection.HOME ->
                    HomeScreen {
                        selected = it
                    }

                AppSection.ENCYCLOPEDIA ->
                    EncyclopediaScreen()

                AppSection.TEACHER ->
                    TeacherScreen()

                AppSection.CALCULATOR ->
                    CalculatorScreen()

                AppSection.GRAPHS ->
                    GraphScreen()

                AppSection.QUIZ ->
                    QuizScreen()

                AppSection.NOTEBOOK ->
                    NotebookScreen()

                AppSection.GEOMETRY ->
                    GeometryScreen()

                AppSection.PROGRESS ->
                    ProgressScreen()

                AppSection.SETTINGS ->
                    SettingsScreen()
            }
        }

        NavigationBar(
            containerColor = Color(0xFF0B111D),
            contentColor = White
        ) {

            val navItems = listOf(
                AppSection.HOME,
                AppSection.ENCYCLOPEDIA,
                AppSection.CALCULATOR,
                AppSection.NOTEBOOK,
                AppSection.SETTINGS
            )

            navItems.forEach { item ->

                NavigationBarItem(
                    selected = selected == item,
                    onClick = {
                        selected = item
                    },
                    icon = {
                        Text(item.icon, fontSize = 20.sp)
                    },
                    label = {
                        Text(item.title, fontSize = 9.sp)
                    },
                    colors = NavigationBarItemDefaults.colors(
                        selectedIconColor = Neon,
                        selectedTextColor = Neon,
                        indicatorColor = Color(0xFF18313A),
                        unselectedIconColor = Muted,
                        unselectedTextColor = Muted
                    )
                )
            }
        }
    }
}

@Composable
private fun Header(onMenu: () -> Unit) {

    Row(
        Modifier
            .fillMaxWidth()
            .background(Background)
            .padding(16.dp),
        verticalAlignment = Alignment.CenterVertically
    ) {

        Text(
            "☰",
            color = Neon,
            fontSize = 24.sp,
            modifier = Modifier.clickable {
                onMenu()
            }
        )

        Spacer(Modifier.width(12.dp))

        Column(
            Modifier.weight(1f)
        ) {

            Text(
                "عالم الرياضيات",
                color = White,
                fontSize = 20.sp,
                fontWeight = FontWeight.Bold
            )

            Text(
                "من الأساسيات إلى الرياضيات المتقدمة",
                color = Muted,
                fontSize = 11.sp
            )
        }

        Text(
            "∑",
            color = Neon,
            fontSize = 28.sp,
            fontWeight = FontWeight.Bold
        )
    }
}

@Composable
private fun Page(
    title: String,
    subtitle: String? = null,
    content: @Composable ColumnScope.() -> Unit
) {

    Column(
        Modifier
            .fillMaxSize()
            .padding(14.dp)
    ) {

        Text(
            title,
            color = Neon,
            fontSize = 21.sp,
            fontWeight = FontWeight.Bold
        )

        if (subtitle != null) {

            Spacer(Modifier.height(4.dp))

            Text(
                subtitle,
                color = Muted,
                fontSize = 12.sp
            )
        }

        Spacer(Modifier.height(12.dp))

        content()
    }
}

@Composable
private fun PanelCard(
    content: @Composable ColumnScope.() -> Unit
) {

    Column(
        Modifier
            .fillMaxWidth()
            .border(
                1.dp,
                Color(0xFF24545B),
                RoundedCornerShape(14.dp)
            )
            .background(
                Panel,
                RoundedCornerShape(14.dp)
            )
            .padding(14.dp),
        content = content
    )
}

@Composable
private fun HomeScreen(
    onSelect: (AppSection) -> Unit
) {

    Page(
        "مرحباً بك في عالم الرياضيات",
        "مساحة تعليمية للشرح والتدريب والاستكشاف"
    ) {

        PanelCard {

            Text(
                "ابدأ رحلتك الرياضية",
                color = White,
                fontSize = 17.sp,
                fontWeight = FontWeight.Bold
            )

            Spacer(Modifier.height(6.dp))

            Text(
                "اختر القسم الذي تريد العمل عليه.",
                color = Muted
            )
        }

        Spacer(Modifier.height(12.dp))

        val cards = listOf(
            AppSection.ENCYCLOPEDIA,
            AppSection.TEACHER,
            AppSection.CALCULATOR,
            AppSection.GRAPHS,
            AppSection.QUIZ,
            AppSection.NOTEBOOK,
            AppSection.GEOMETRY,
            AppSection.PROGRESS
        )

        LazyColumn(
            verticalArrangement = Arrangement.spacedBy(9.dp)
        ) {

            items(cards) { item ->

                PanelCard {

                    Row(
                        Modifier
                            .fillMaxWidth()
                            .clickable {
                                onSelect(item)
                            },
                        verticalAlignment = Alignment.CenterVertically
                    ) {

                        Text(
                            item.icon,
                            color = Neon,
                            fontSize = 25.sp
                        )

                        Spacer(Modifier.width(12.dp))

                        Text(
                            item.title,
                            color = White,
                            fontWeight = FontWeight.SemiBold,
                            modifier = Modifier.weight(1f)
                        )

                        Text(
                            "←",
                            color = Neon,
                            fontSize = 20.sp
                        )
                    }
                }
            }
        }
    }
}

@Composable
private fun EncyclopediaScreen() {

    val categories = listOf(

        LessonCategory(
            "المرحلة الابتدائية",
            listOf(
                "الأعداد والعمليات الحسابية",
                "الكسور والأعداد العشرية",
                "النسبة والتناسب",
                "القياس"
            )
        ),

        LessonCategory(
            "المرحلة المتوسطة",
            listOf(
                "الجبر الأساسي",
                "المعادلات والمتباينات",
                "الهندسة والمحيط والمساحة",
                "الإحصاء والاحتمالات"
            )
        ),

        LessonCategory(
            "المرحلة الثانوية",
            listOf(
                "الدوال والتمثيل البياني",
                "المثلثات",
                "الأسس واللوغاريتمات",
                "المتتاليات"
            )
        ),

        LessonCategory(
            "المرحلة الجامعية",
            listOf(
                "النهايات والاستمرارية",
                "التفاضل",
                "التكامل",
                "الجبر الخطي"
            )
        ),

        LessonCategory(
            "الرياضيات المتقدمة",
            listOf(
                "التحليل الحقيقي",
                "التحليل العقدي",
                "الطوبولوجيا",
                "المعادلات التفاضلية"
            )
        ),

        LessonCategory(
            "موضوعات تخصصية",
            listOf(
                "نظرية الأعداد",
                "نظرية المجموعات",
                "الرياضيات التطبيقية",
                "الاحتمالات المتقدمة"
            )
        )
    )

    Page(
        "الموسوعة الرياضية",
        "تصنيف قابل للتوسعة إلى آلاف الموضوعات"
    ) {

        LazyColumn(
            verticalArrangement = Arrangement.spacedBy(10.dp)
        ) {

            items(categories) { category ->

                PanelCard {

                    Text(
                        category.level,
                        color = Neon,
                        fontWeight = FontWeight.Bold,
                        fontSize = 16.sp
                    )

                    Spacer(Modifier.height(6.dp))

                    category.topics.forEach { topic ->

                        var expanded by remember {
                            mutableStateOf(false)
                        }

                        Column {

                            Text(
                                "• $topic",
                                color = White,
                                modifier = Modifier
                                    .fillMaxWidth()
                                    .clickable {
                                        expanded = !expanded
                                    }
                                    .padding(vertical = 7.dp)
                            )

                            if (expanded) {

                                Text(
                                    "سيضاف هنا شرح الدرس والقواعد والأمثلة المحلولة والتمارين.",
                                    color = Muted,
                                    fontSize = 12.sp,
                                    modifier = Modifier.padding(
                                        start = 12.dp,
                                        bottom = 8.dp
                                    )
                                )
                            }
                        }
                    }
                }
            }
        }
    }
}

@Composable
private fun TeacherScreen() {

    var question by remember {
        mutableStateOf("")
    }

    var answer by remember {
        mutableStateOf(
            "اكتب مسألتك الرياضية هنا. هذه الواجهة تحتاج إلى ربط نموذج ذكاء اصطناعي محلي لتوليد الإجابات."
        )
    }

    Page(
        "المعلم الرياضي الذكي",
        "شرح المسائل خطوة بخطوة"
    ) {

        PanelCard {

            Text(
                "اكتب السؤال الرياضي",
                color = Neon,
                fontWeight = FontWeight.Bold
            )

            Spacer(Modifier.height(8.dp))

            BasicTextField(
                value = question,
                onValueChange = {
                    question = it
                },
                modifier = Modifier
                    .fillMaxWidth()
                    .background(
                        Color(0xFF080D16),
                        RoundedCornerShape(8.dp)
                    )
                    .padding(12.dp),
                textStyle = androidx.compose.ui.text.TextStyle(
                    color = White,
                    fontSize = 15.sp
                ),
                decorationBox = { inner ->

                    if (question.isEmpty()) {

                        Text(
                            "مثال: حل المعادلة س² - ٥س + ٦ = ٠",
                            color = Muted
                        )
                    }

                    inner()
                }
            )

            Spacer(Modifier.height(10.dp))

            Button(
                onClick = {

                    answer = if (question.isBlank()) {

                        "يرجى كتابة سؤال أولاً."

                    } else {

                        "تم استلام السؤال:\n$question\n\nلم يتم ربط نموذج الذكاء الاصطناعي المحلي بعد."
                    }
                }
            ) {

                Text("تحليل السؤال")
            }
        }

        Spacer(Modifier.height(12.dp))

        PanelCard {

            Text(
                "مساحة الشرح والحل",
                color = Neon,
                fontWeight = FontWeight.Bold
            )

            Spacer(Modifier.height(8.dp))

            Text(
                answer,
                color = White,
                lineHeight = 23.sp
            )
        }
    }
}

@Composable
private fun CalculatorScreen() {

    var expression by remember {
        mutableStateOf("")
    }

    var result by remember {
        mutableStateOf("ستظهر النتيجة هنا")
    }

    Page(
        "الحاسبة الرياضية",
        "أدخل تعبيراً حسابياً"
    ) {

        PanelCard {

            BasicTextField(
                value = expression,
                onValueChange = {
                    expression = it
                },
                modifier = Modifier
                    .fillMaxWidth()
                    .background(
                        Color(0xFF080D16),
                        RoundedCornerShape(8.dp)
                    )
                    .padding(12.dp),
                textStyle = androidx.compose.ui.text.TextStyle(
                    color = White,
                    fontSize = 18.sp
                )
            )

            Spacer(Modifier.height(12.dp))

            Row(
                horizontalArrangement = Arrangement.spacedBy(8.dp)
            ) {

                Button(
                    onClick = {

                        result = try {

                            val value = Expression(expression).calculate()

                            if (value.isNaN() || value.isInfinite()) {
                                "تعذر حساب التعبير"
                            } else {
                                value.toString()
                            }

                        } catch (_: Exception) {

                            "تعبير غير صالح"
                        }
                    }
                ) {

                    Text("احسب")
                }

                OutlinedButton(
                    onClick = {
                        expression = ""
                        result = "ستظهر النتيجة هنا"
                    }
                ) {

                    Text("مسح")
                }
            }
        }

        Spacer(Modifier.height(12.dp))

        PanelCard {

            Text(
                "النتيجة",
                color = Neon,
                fontWeight = FontWeight.Bold
            )

            Spacer(Modifier.height(8.dp))

            Text(
                result,
                color = White,
                fontSize = 22.sp
            )
        }
    }
}

@Composable
private fun GraphScreen() {

    var function by remember {
        mutableStateOf("sin(x)")
    }

    var points by remember {
        mutableStateOf<List<Offset>>(emptyList())
    }

    Page(
        "مختبر الرسوم البيانية",
        "رسم تقريبي للدوال"
    ) {

        PanelCard {

            BasicTextField(
                value = function,
                onValueChange = {
                    function = it
                },
                modifier = Modifier
                    .fillMaxWidth()
                    .background(
                        Color(0xFF080D16),
                        RoundedCornerShape(8.dp)
                    )
                    .padding(10.dp),
                textStyle = androidx.compose.ui.text.TextStyle(
                    color = White,
                    fontSize = 16.sp
                )
            )

            Spacer(Modifier.height(8.dp))

            Button(
                onClick = {

                    points = (0..240).mapNotNull { i ->

                        val x = (i - 120) / 12.0

                        val y = try {

                            Expression(
                                function.replace("x", "($x)")
                            ).calculate()

                        } catch (_: Exception) {

                            Double.NaN
                        }

                        if (y.isFinite() && abs(y) < 100) {
                            Offset(i.toFloat(), y.toFloat())
                        } else {
                            null
                        }
                    }
                }
            ) {

                Text("ارسم الدالة")
            }
        }

        Spacer(Modifier.height(12.dp))

        PanelCard {

            Canvas(
                Modifier
                    .fillMaxWidth()
                    .height(260.dp)
                    .background(Color(0xFF080D16))
            ) {

                val midY = size.height / 2f
                val midX = size.width / 2f

                drawLine(
                    Muted,
                    Offset(0f, midY),
                    Offset(size.width, midY),
                    1f
                )

                drawLine(
                    Muted,
                    Offset(midX, 0f),
                    Offset(midX, size.height),
                    1f
                )

                if (points.size > 1) {

                    val scaleX = size.width / 240f
                    val scaleY = 12f

                    points.zipWithNext().forEach { (a, b) ->

                        drawLine(
                            Neon,
                            Offset(
                                a.x * scaleX,
                                midY - a.y * scaleY
                            ),
                            Offset(
                                b.x * scaleX,
                                midY - b.y * scaleY
                            ),
                            2f,
                            cap = StrokeCap.Round
                        )
                    }
                }
            }
        }
    }
}

@Composable
private fun QuizScreen() {

    var selected by remember {
        mutableIntStateOf(-1)
    }

    var checked by remember {
        mutableStateOf(false)
    }

    val options = listOf("٢", "٣", "٤", "٥")

    Page(
        "الاختبارات والتدريبات",
        "اختبار تجريبي"
    ) {

        PanelCard {

            Text(
                "ما قيمة ٧ - ٤ ؟",
                color = White,
                fontSize = 19.sp,
                fontWeight = FontWeight.Bold
            )

            Spacer(Modifier.height(12.dp))

            options.forEachIndexed { index, option ->

                Row(
                    Modifier
                        .fillMaxWidth()
                        .clickable {
                            selected = index
                            checked = false
                        }
                        .padding(vertical = 7.dp),
                    verticalAlignment = Alignment.CenterVertically
                ) {

                    RadioButton(
                        selected = selected == index,
                        onClick = {
                            selected = index
                            checked = false
                        }
                    )

                    Text(
                        option,
                        color = White
                    )
                }
            }

            Button(
                onClick = {
                    checked = true
                },
                enabled = selected >= 0
            ) {

                Text("تحقق من الإجابة")
            }

            if (checked) {

                Text(
                    if (selected == 1) {
                        "إجابة صحيحة!"
                    } else {
                        "إجابة غير صحيحة، حاول مرة أخرى."
                    },
                    color = if (selected == 1) Neon else Purple
                )
            }
        }
    }
}

@Composable
private fun NotebookScreen() {

    val context = LocalContext.current

    var note by remember {

        mutableStateOf(
            context
                .getSharedPreferences("math_world", 0)
                .getString("note", "") ?: ""
        )
    }

    var status by remember {
        mutableStateOf("")
    }

    Page(
        "دفتر الرياضيات",
        "احفظ ملاحظاتك على الجهاز"
    ) {

        PanelCard {

            BasicTextField(
                value = note,
                onValueChange = {
                    note = it
                },
                modifier = Modifier
                    .fillMaxWidth()
                    .height(220.dp)
                    .background(
                        Color(0xFF080D16),
                        RoundedCornerShape(8.dp)
                    )
                    .padding(12.dp),
                textStyle = androidx.compose.ui.text.TextStyle(
                    color = White,
                    fontSize = 15.sp,
                    lineHeight = 23.sp
                ),
                decorationBox = { inner ->

                    if (note.isEmpty()) {

                        Text(
                            "اكتب القوانين والملاحظات هنا...",
                            color = Muted
                        )
                    }

                    inner()
                }
            )

            Spacer(Modifier.height(10.dp))

            Button(
                onClick = {

                    context
                        .getSharedPreferences("math_world", 0)
                        .edit()
                        .putString("note", note)
                        .apply()

                    status = "تم حفظ الملاحظة."
                }
            ) {

                Text("حفظ الملاحظة")
            }

            Text(
                status,
                color = Neon,
                fontSize = 12.sp
            )
        }
    }
}

@Composable
private fun GeometryScreen() {

    var radius by remember {
        mutableStateOf("5")
    }

    val r = radius.toDoubleOrNull()

    Page(
        "الهندسة التفاعلية",
        "حسابات هندسية أولية"
    ) {

        PanelCard {

            Text(
                "مساحة الدائرة",
                color = Neon,
                fontWeight = FontWeight.Bold
            )

            Text(
                "المساحة = π × نق²",
                color = White,
                fontSize = 20.sp
            )

            Spacer(Modifier.height(8.dp))

            BasicTextField(
                value = radius,
                onValueChange = {
                    radius = it
                },
                modifier = Modifier
                    .fillMaxWidth()
                    .background(
                        Color(0xFF080D16),
                        RoundedCornerShape(8.dp)
                    )
                    .padding(10.dp),
                textStyle = androidx.compose.ui.text.TextStyle(
                    color = White,
                    fontSize = 17.sp
                )
            )

            Spacer(Modifier.height(8.dp))

            Text(
                if (r != null && r >= 0) {
                    "المساحة ≈ ${"%.4f".format(Math.PI * r * r)}"
                } else {
                    "أدخل نصف قطر صحيحاً"
                },
                color = Neon,
                fontSize = 18.sp
            )

            Spacer(Modifier.height(14.dp))

            Canvas(
                Modifier
                    .fillMaxWidth()
                    .height(170.dp)
            ) {

                val rad = min(size.width, size.height) * 0.34f

                drawCircle(
                    Neon,
                    rad,
                    Offset(
                        size.width / 2f,
                        size.height / 2f
                    ),
                    style = androidx.compose.ui.graphics.drawscope.Stroke(3f)
                )

                drawLine(
                    Purple,
                    Offset(
                        size.width / 2f,
                        size.height / 2f
                    ),
                    Offset(
                        size.width / 2f + rad,
                        size.height / 2f
                    ),
                    2f
                )
            }
        }
    }
}

@Composable
private fun ProgressScreen() {

    Page(
        "متابعة التقدم",
        "ملخص نشاطك داخل التطبيق"
    ) {

        PanelCard {

            Text(
                "دفتر الرياضيات",
                color = Neon,
                fontWeight = FontWeight.Bold
            )

            Text(
                "يمكنك حفظ ملاحظاتك والعودة إليها.",
                color = White
            )
        }

        Spacer(Modifier.height(10.dp))

        PanelCard {

            Text(
                "الاختبارات",
                color = Neon,
                fontWeight = FontWeight.Bold
            )

            Text(
                "سيتم إضافة سجل الدرجات والإحصاءات لاحقاً.",
                color = White
            )
        }

        Spacer(Modifier.height(10.dp))

        PanelCard {

            Text(
                "الدروس المكتملة",
                color = Neon,
                fontWeight = FontWeight.Bold
            )

            Text(
                "سيضاف نظام تتبع الدروس في مرحلة التطوير التالية.",
                color = White
            )
        }
    }
}

@Composable
private fun SettingsScreen() {

    val context = LocalContext.current

    var modelStatus by remember {
        mutableStateOf("لم يتم اختيار نموذج محلي.")
    }

    val modelPicker =
        rememberLauncherForActivityResult(
            ActivityResultContracts.OpenDocument()
        ) { uri: Uri? ->

            if (uri != null) {

                try {

                    val destination = File(
                        context.filesDir,
                        "local-model.gguf"
                    )

                    context.contentResolver
                        .openInputStream(uri)
                        ?.use { input ->

                            FileOutputStream(destination).use { output ->
                                input.copyTo(output)
                            }
                        }

                    modelStatus =
                        "تم نسخ ملف النموذج. لم يتم تشغيله بعد."

                } catch (e: Exception) {

                    modelStatus =
                        "تعذر نسخ الملف: ${e.message}"
                }
            }
        }

    Page(
        "الإعدادات",
        "إعدادات التشغيل المحلي"
    ) {

        PanelCard {

            Text(
                "نموذج الذكاء الاصطناعي المحلي",
                color = Neon,
                fontWeight = FontWeight.Bold
            )

            Spacer(Modifier.height(6.dp))

            Text(
                "اختر ملف نموذج بصيغة GGUF. يلزم دمج مشغّل مثل llama.cpp لتشغيل النموذج فعلياً.",
                color = White
            )

            Spacer(Modifier.height(10.dp))

            Button(
                onClick = {
                    modelPicker.launch(arrayOf("*/*"))
                }
            ) {

                Text("اختيار ملف النموذج")
            }

            Spacer(Modifier.height(8.dp))

            Text(
                modelStatus,
                color = Muted,
                fontSize = 12.sp
            )
        }

        Spacer(Modifier.height(10.dp))

        PanelCard {

            Text(
                "عرض المعادلات الأكاديمية",
                color = Neon,
                fontWeight = FontWeight.Bold
            )

            Text(
                "يلزم إضافة MathJax محلياً لعرض الكسور والجذور والمصفوفات والمعادلات بصيغة LaTeX.",
                color = White
            )
        }

        Spacer(Modifier.height(10.dp))

        PanelCard {

            Text(
                "العمل دون إنترنت",
                color = Neon,
                fontWeight = FontWeight.Bold
            )

            Text(
                "الواجهة والدفتر والحاسبة الأولية تعمل محلياً. تشغيل الذكاء الاصطناعي يحتاج ملفات التشغيل والنموذج.",
                color = White
            )
        }
    }
}
