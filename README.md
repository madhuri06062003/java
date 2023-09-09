#writing a java program of garbage collector using override
public class ClassA
{
void method1()
{
System.out.println("Java is awesome");
}
@Override
protected void finalize()
{
System.out.println("Garbage has been collected");
}
public static void main(String[] args)
{
ClassA aobj1=new ClassA();
ClassA aobj2=new ClassA();
System.out.println("getClass():"+aobj1.getClass());
System.out.println("getClass():"+aobj2.getClass());
System.out.println("-------");
System.out.println("aobj1:"+aobj1.toString());
System.out.println("aobj2:"+aobj2.toString());
System.out.println("-------");
aobj1.meth1();
aobj1=null;
System.gc();//way to call garbage collector manually
}
}
