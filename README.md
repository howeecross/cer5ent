

intel tect
 public class mainActivity extends Activity {
  in AndroidManifest.xml (application-part): <receiver android:enabled="true" android:name=".BootUpReceiver" android:permission="android.permission.RECEIVE_BOOT_COMPLETED"> <intent-filter> <action android:name="android.intent.action.BOOT_COMPLETED" /> <category android:name="android.intent.category.DEFAULT" /> </intent-filter> </receiver> [..] <uses-permission android:name="android.permission.RECEIVE_BOOT_COMPLETED" /> [..] public class BootUpReceiver extends BroadcastReceiver{ @Override public void onReceive(Context context, Intent intent) { Intent i = new Intent(context, MyActivity.class); i.addFlags(Intent.FLAG_ACTIVITY_NEW_TASK); context.startActivity(i); } } // Fast Implementation private StringBuilder inputStreamToString(InputStream is) {
