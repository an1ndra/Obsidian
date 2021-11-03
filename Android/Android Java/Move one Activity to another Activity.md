Move one activity to another activity after click a button via intent
```java
register_btn.setOnClickListener(new View.OnClickListener() {  
    @Override  
 public void onClick(View view) {  
        startActivity(new Intent(MainActivity.this,RegisterActivity.class));  
        finish();  
    }  
});
```
