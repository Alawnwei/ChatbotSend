package messageManager;

import org.apache.http.HttpResponse;
import org.apache.http.HttpStatus;
import org.apache.http.client.HttpClient;
import org.apache.http.client.methods.HttpPost;
import org.apache.http.entity.StringEntity;
import org.apache.http.impl.client.HttpClients;
import org.apache.http.util.EntityUtils;

public class ChatbotSend {
	 
    public static String WEBHOOK_TOKEN = "https://oapi.dingtalk.com/robot/send?access_token=012399dff2523cfeb5918bcf2ba9cc3b3bfc44b267fb19145ba3a8eabf224e0c";
 
    public static void main(String args[]) throws Exception{
 
        HttpClient httpclient = HttpClients.createDefault();
 
        HttpPost httppost = new HttpPost(WEBHOOK_TOKEN);
        httppost.addHeader("Content-Type", "application/json; charset=utf-8");
 
        String textMsg = "{ \"msgtype\": \"text\", \"text\": {\"content\": \"QA TEST\"}}";
        StringEntity se = new StringEntity(textMsg, "utf-8");
        httppost.setEntity(se);
 
        HttpResponse response = httpclient.execute(httppost);
        if (response.getStatusLine().getStatusCode()== HttpStatus.SC_OK){
            String result= EntityUtils.toString(response.getEntity(), "utf-8");
            System.out.println(result);
        }
    }
}
