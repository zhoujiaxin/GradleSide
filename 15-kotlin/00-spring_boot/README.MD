Hello Kotlin~

`Kotlin`��ʽ����֮�������˲���Ŀ��,����`Gradle`��3.5�汾��ʱ���Ƴ��˻���`Gradle`��dsl.
�����׵�`jetbrains`,���иɵ�`google`,������û�˹�ע����.

����չʾ�������`Gradle`������һ������`Kotlin`��`Srping Boot`��Ŀ.
> p.s �ð�,�ҳ��ϼ�spring boot������Ϊ�˲�������ȶȵ�

1.��Ŀ�ṹ
src
    |-main
        |-kotlin

�������`src/main/java`��Ҳ�ǿ��Ե�

2.�����ű�

```groovy
// Ӧ��kotlin���
plugins {
    id "org.jetbrains.kotlin.jvm" version "1.1.3-2"
}
// ����汾��
ext{
    kotlin_version = '1.1.2-4'
}
// ����ֿ�
repositories {
    mavenLocal()
    maven { url"https://repo.spring.io/libs-release" }
    jcenter()
    mavenCentral()
}

dependencies {
    // kotlin��׼��֧��
    compile "org.jetbrains.kotlin:kotlin-stdlib:$kotlin_version"
    // �����java8�淶�ֽ���
    compile "org.jetbrains.kotlin:kotlin-stdlib-jre8:$kotlin_version"
    // ...��������

}
```