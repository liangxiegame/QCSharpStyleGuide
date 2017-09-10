#### ProgramingStyle

~~~c#
namespace QFramework.Example 
{	
	using UnityEngine;
	using UnityEngine.UI;
	using System.Collections;
	using System.Collections.Generic;
	
	/// <summary>
	/// 展示编码风格
	/// </summary>
	public class ProgrammingStyle : MonoBehaviour 
	{
		#region Basic App
		/// <summary>
		/// 1.private/protected使用m开头+驼峰式
		/// 2.前缀最好展示所属的Component类型比如Button->Btn
		/// </summary>
		[SerializeField] Button mBtnEnterMainPage;

		/// <summary>
		/// public类型使用首字母大写驼峰式
		/// </summary>
		public int LastIndex = 0;

		/// <summary>
		/// public 类型属性也算public类型变量
		/// </summary>
		public int CurSelectIndex 
		{
			get { return mCurSelectIndex; }
		}

		void Start () 
		{
			mBtnEnterMainPage = transform.Find ("BtnEnterMainPage").GetComponent<Button>();

			// GameObject命名
			// 临时变量命名采用首字母小写驼峰式
			GameObject firstPosGo = transform.Find ("FirstPosGo").gameObject;
		}

		/// <summary>
		/// 方法名一律首字母大写驼峰式
		/// </summary>
		public void Hide() 
		{
			gameObject.SetActive (false);
		}
		#endregion

		#region Advanced
		/*
		 * GameObject->Go
		 * Transform->Trans
		 * Button->Btn
		 * 
		 * For->4
		 * To->2
		 * Dictionary->Dict
		 * Number->Num
		 * Current->Cur
		 */

		/// <summary>
		/// 1.Bg肯定是图片
		/// </summary>
		[SerializeField] Image mBg;

		/// <summary>
		/// GameObject->Go
		/// </summary>
		[SerializeField] GameObject mDialogGo;

		/// <summary>
		/// Transfom->Trans
		/// </summary>
		[SerializeField] Transform mScrollViewTrans;

		/// <summary>
		/// Index、Num、Count等肯定是int
		/// </summary>
		[SerializeField] int mCurSelectIndex;

		/// <summary>
		/// RectTransform->RectTrans;
		/// </summary>
		[SerializeField] RectTransform mScrollContentRectTrans;

		/// <summary>
		/// 1.Pos肯定是Vector3、Vector2
		/// 2.Size肯定是Vector2
		/// </summary>
		[SerializeField] Vector3 mCachedPos;
		[SerializeField] Vector2 mCachedSize;

		/// <summary>
		/// 后缀s表示是个数组
		/// </summary>
		[SerializeField] Vector3[] mCachedPositions;

		/// <summary>
		/// 1.List后缀
		/// 2.4->for 表示所属关系可以表示Dict
		/// 3.Dict后置
		/// </summary>
		[SerializeField] List<Vector3> mCachedPosList;
		[SerializeField] Dictionary<string,Vector3> mPos4ChildName;
		[SerializeField] Dictionary<string,Vector3> mChildPosDict;
		#endregion
	}
}
~~~

