public class Singleton{
	private static final volatile Singleton INSTANCE;
	
	private Singleton(){
	}
	
	public static getInstance(){
		if(INSTANCE==null){
			synchrnozied(Singleton.class){
				return new INSTANCE();
			}
		}
		return INSTANCE;
	}

}