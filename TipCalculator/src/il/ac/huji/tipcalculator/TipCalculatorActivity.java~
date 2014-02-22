package il.ac.huji.tipcalculator;

import il.ac.huji.tipcalculator.R.id;
import android.os.Bundle;
import android.app.Activity;
import android.view.Menu;
import android.view.View;
import android.widget.Button;
import android.widget.CheckBox;
import android.widget.EditText;

public class TipCalculatorActivity extends Activity {

	@Override
	protected void onCreate(Bundle savedInstanceState) {
		super.onCreate(savedInstanceState);
		setContentView(R.layout.activity_tip_calculator);
		 final Button Calculate = (Button) findViewById(R.id.btnCalculate);
		 final EditText tip = (EditText) findViewById(R.id.txtTipResult);
		 final EditText amount =(EditText) findViewById(R.id.amount);
		 final CheckBox round = (CheckBox) findViewById(R.id.chkRound);
         Calculate.setOnClickListener(new View.OnClickListener() {
             public void onClick(View v) {
            	 
                 if (round.isChecked()) {
                	 String sum1 = amount.getText().toString(); 
                	 double sum = Double.parseDouble(sum1);
                	 sum=sum*0.15;
                	 if (sum - Math.floor(sum) >=0.5) {
                		 sum = Math.ceil(sum);
                		 }else{
                		 sum = Math.floor(sum);
                		 } 
                	 tip.setText("$"+String.valueOf(sum));
                 }else{
            	      String sum1 = amount.getText().toString();
            	      double sum = Double.parseDouble(sum1);
            	      tip.setText("$"+String.valueOf(sum*0.15));
                 }
             }

         });

	 }
	

	@Override
	public boolean onCreateOptionsMenu(Menu menu) {
		// Inflate the menu; this adds items to the action bar if it is present.
		getMenuInflater().inflate(R.menu.tip_calculator, menu);
		return true;
	}

}
