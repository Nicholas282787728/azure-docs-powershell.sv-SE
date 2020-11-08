---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: B9153CA9-06D1-4EF3-9863-D649C2EBAEAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermvpnclientrootcertificate
schema: 2.0.0
ms.openlocfilehash: 2f5d73cd06d975d6458776dee4242b392b5c160b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931353"
---
# <span data-ttu-id="6f7bd-101">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6f7bd-101">Add-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="6f7bd-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f7bd-102">SYNOPSIS</span></span>
<span data-ttu-id="6f7bd-103">Lägger till en VPN-klient rot certifikat.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-103">Adds a VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f7bd-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f7bd-104">SYNTAX</span></span>

```
Add-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String> -VirtualNetworkGatewayName <String>
 -ResourceGroupName <String> -PublicCertData <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f7bd-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f7bd-105">DESCRIPTION</span></span>
<span data-ttu-id="6f7bd-106">Cmdleten **Add-AzureRmVpnClientRootCertificate** lägger till ett rot certifikat till en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-106">The **Add-AzureRmVpnClientRootCertificate** cmdlet adds a root certificate to a virtual network gateway.</span></span>
<span data-ttu-id="6f7bd-107">Rot certifikat är 509 certifikat som identifierar din rot certifikat utfärdare.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-107">Root certificates are X.509 certificates that identify your Root Certification Authority.</span></span>
<span data-ttu-id="6f7bd-108">Efter design är rot certifikatet som används på gatewayen.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-108">By design, all certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="6f7bd-109">Denna cmdlet tilldelar ett befintligt certifikat som ett Gateway-rotcertifikat.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-109">This cmdlet assigns an existing certificate as a gateway root certificate.</span></span>
<span data-ttu-id="6f7bd-110">Om du inte har något 509-certifikat tillgängligt kan du skapa ett via din offentliga infrastruktur eller använda en certifikat generator, till exempel makecert.exe.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-110">If you do not have an X.509 certificate available you can generate one through your public key infrastructure or use a certificate generator such as makecert.exe.</span></span>

<span data-ttu-id="6f7bd-111">Om du vill lägga till ett rot certifikat måste du ange certifikat namnet och tillhandahålla en representation av certifikatet (se *PublicCertData* -parametern för mer information).</span><span class="sxs-lookup"><span data-stu-id="6f7bd-111">To add a root certificate, you must specify the certificate name and provide a text-only representation of the certificate (see *the PublicCertData* parameter for more information).</span></span>
<span data-ttu-id="6f7bd-112">Med Azure kan du tilldela mer än ett rot certifikat till en gateway.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-112">Azure allows you to assign more than one root certificate to a gateway.</span></span>
<span data-ttu-id="6f7bd-113">Flera rot certifikat distribueras ofta av organisationer som innehåller användare från mer än ett företag.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-113">Multiple root certificates are often deployed by organizations that include users from more than one company.</span></span>

## <span data-ttu-id="6f7bd-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f7bd-114">EXAMPLES</span></span>

### <span data-ttu-id="6f7bd-115">Exempel 1: lägga till ett klient rot certifikat till en virtuell gateway</span><span class="sxs-lookup"><span data-stu-id="6f7bd-115">Example 1: Add a client root certificate to a virtual gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Add-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway" -VpnClientRootCertificateName "ContosoClientRootCertificate"
```

<span data-ttu-id="6f7bd-116">Det här exemplet lägger till ett klient rot certifikat till en virtuell gateway med namnet ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-116">This example adds a client root certificate to a virtual gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="6f7bd-117">I det första kommandot används cmdleten **Get-Content** för att få en tidigare exporterad text av rot certifikatet och lagrar text data som variabeln $text.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-117">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the root certificate and stores that text data the variable named $Text.</span></span>

<span data-ttu-id="6f7bd-118">Det andra kommandot använder sedan en for-slinga för att extrahera all text förutom den första raden och den sista raden.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-118">The second command then uses a for loop to extract all the text except for the first line and the last line.</span></span>
<span data-ttu-id="6f7bd-119">Den extraherade texten lagras i en variabel som heter $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-119">The extracted text is stored in a variable named $CertificateText.</span></span>

<span data-ttu-id="6f7bd-120">Det tredje kommandot använder sedan den text som lagras i $CertificateText med cmdleten **Add-AzureRmVpnClientRootCertificate** för att lägga till rot certifikatet till gatewayen.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-120">The third command then uses the text stored in $CertificateText with the **Add-AzureRmVpnClientRootCertificate** cmdlet to add the root certificate to the gateway.</span></span>

## <span data-ttu-id="6f7bd-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f7bd-121">PARAMETERS</span></span>

### <span data-ttu-id="6f7bd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f7bd-122">-DefaultProfile</span></span>
<span data-ttu-id="6f7bd-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f7bd-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="6f7bd-124">-PublicCertData</span></span>
<span data-ttu-id="6f7bd-125">Anger text representationen för det rot certifikat som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-125">Specifies the text representation of the root certificate to be added.</span></span>
<span data-ttu-id="6f7bd-126">För att få text presentationen exporterar du certifikatet i CER-format (med base64-kodning) och öppnar sedan den resulterande filen i en text redigerare.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="6f7bd-127">När du gör det visas utdata som liknar följande (Observera att den faktiska utmatningen innehåller många fler text rader än det förkortade provet här):</span><span class="sxs-lookup"><span data-stu-id="6f7bd-127">When you do that, you will see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="6f7bd-128">-----Starta certifikat----------avsluta certifikat-----</span><span class="sxs-lookup"><span data-stu-id="6f7bd-128">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="6f7bd-129">PublicCertData består av alla rader mellan den första raden (-----BEGIN CERTIFICATe-----) och den sista raden (-----slut certifikatet-----) i filen.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-129">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="6f7bd-130">Du kan hämta dessa data genom att använda Windows PowerShell-kommandon som det här: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span><span class="sxs-lookup"><span data-stu-id="6f7bd-130">You can retrieve this data  by using Windows PowerShell commands similar to this: `$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"`
`$CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}`</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7bd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f7bd-131">-ResourceGroupName</span></span>
<span data-ttu-id="6f7bd-132">Anger namnet på resurs gruppen som rot certifikatet är tilldelat till.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-132">Specifies the name of the resource group that the root certificate is assigned to.</span></span>

<span data-ttu-id="6f7bd-133">Resurs grupper kategoriserar artiklar för att förenkla lager hantering och allmän Azure-administration.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-133">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7bd-134">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="6f7bd-134">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="6f7bd-135">Anger namnet på den virtuella nätverksgateway där certifikatet läggs till.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-135">Specifies the name of the virtual network gateway where the certificate is added.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7bd-136">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="6f7bd-136">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="6f7bd-137">Anger namnet på klient rot certifikatet som läggs till av denna cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-137">Specifies the name of the client root certificate that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f7bd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f7bd-138">CommonParameters</span></span>
<span data-ttu-id="6f7bd-139">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f7bd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f7bd-140">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f7bd-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f7bd-141">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f7bd-141">INPUTS</span></span>

## <span data-ttu-id="6f7bd-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f7bd-142">OUTPUTS</span></span>

### <span data-ttu-id="6f7bd-143">Microsoft. Azure. commands. Networks. Models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6f7bd-143">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="6f7bd-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f7bd-144">NOTES</span></span>

## <span data-ttu-id="6f7bd-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f7bd-145">RELATED LINKS</span></span>

[<span data-ttu-id="6f7bd-146">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6f7bd-146">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="6f7bd-147">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6f7bd-147">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="6f7bd-148">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6f7bd-148">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)

