public class FutureExample{

	public static voi
	d main(String[] args) throws Exception{
		ExecutorService executor = Executors.newSingleThreadExecutor();
		
		Callable<String> task = ()->{
			Thread.sleep(1000);
			return "Task Completed";
		}
		
		Future<String> future = executor.submit(task);
		
		String result = future.get();
		System.out.println(result);
		
		executor.shutdown();
	}

}