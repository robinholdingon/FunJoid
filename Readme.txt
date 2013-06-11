Test
version 2

ArrayList<LinkList<treeNode>> getLevelLinkList(treeNode root)
{
	ArrayList<LinkList<treeNode>> results = new...;
	LinkList<treeNode> current = new...;
	
	current.add(root);
	while(!current.empty())
	{
		results.add(current);
		LinkList<treeNode> parents = current;
		current = new LinkList<treeNode>;
		for(treeNode parent : parents)
		{
			if(current.left != null)
				current.add(parent.left);
			if(current.right != null)
				current.add(parent.right);
		}
	}	
}