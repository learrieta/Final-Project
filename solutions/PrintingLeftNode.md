
public class Node {
	public int data;
	public Node left, right;

	public Node(int item)
	{
		data = item;
		left = right = null;
	}
}

public class BinaryTree {
	public Node root;
	public static int max_level = 0;

	// recursive function to print left view
	public virtual void leftViewUtil(Node node, int level)
	{
		// Base Case
		if (node == null) {
			return;
		}

		// If this is the first node of its level
		if (max_level < level) {
			Console.Write(node.data + " ");
			max_level = level;
		}

		// Recur for left and right subtrees
		leftViewUtil(node.left, level + 1);
		leftViewUtil(node.right, level + 1);
	}

	// A wrapper over leftViewUtil()
	public virtual void leftView()
	{
		leftViewUtil(root, 1);
	}

	
	public static void Main(string[] args)
	{
		/* creating a binary tree and entering the nodes */
		BinaryTree tree = new BinaryTree();
		tree.root = new Node(html);
		tree.root.left = new Node(head);
		tree.root.right = new Node(body);
		tree.root.left.left = new Node(meta);
		tree.root.left.right = new Node(title);
		tree.root.right.right = new Node(h2);
		tree.root.right.left = new Node(ul);
		tree.root.right.right.left = new Node(li);

		tree.leftView();
	}
}

