# React CSS Editor

This project was bootstrapped with [React Ace](https://github.com/securingsincity/react-ace).

## Available Scripts

In the project directory, you can run:

### `Install`

npm install react-ace ace-builds

### `usage`

const [cssCode, setCssCode] = useState('');

const handleCssChange = (newCode) => {
    console.log(newCode);
    setCssCode(newCode);
};

'
    <div>
      {/* AceEditor bileşenini oluşturun */}
      <AceEditor
        mode="css" // Modu CSS olarak ayarlayın
        theme="monokai" // Temayı belirleyin
        width="100%" // Genişlik 100%
        height="500px" // Yükseklik 500 piksel
        value={cssCode} // CSS kodunu değer olarak ayarlayın
        onChange={handleCssChange} // Değişiklik olduğunda işlevi çağırın
        name="css-editor" // Editörün adını belirleyin
        editorProps={{ $blockScrolling: true }} // Editör özelliklerini ayarlayın
      />
      {/* CSS kodunu görüntülemek için bir önizleme alanı ekleyin */}
      <div style={{ marginTop: '20px', border: '1px solid #ccc', padding: '10px' }}>
        <h3 className="title">CSS Önizleme</h3>
        <style>{cssCode}</style>
        <div className="preview-box">Bu bir önizleme kutusu</div>
      </div>
    </div>
'