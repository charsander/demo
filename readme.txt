learn git.
newline.
public static String getSubFileName(File file) {
		List<String> list = new ArrayList<String>();
		
		if (file.isDirectory()) {
			System.out.println("该文件夹下所有文件列表如下：");
		
		File[] fileList = file.listFiles();
	
		for (File f : fileList) {
			
			if (f.isFile()) {
				list.add(f.getName());
				for(String c:list){
					System.out.println(c);
				}
			} else {
				//list.addAll(getSubFileName(f));
			}
		}	
	}
		else {
			System.out.println("请输入正确的文件夹路径！");
			System.out.println("请重新输入！");
		}
		return list.toString();
	}
}