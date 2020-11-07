---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: b83af7bc0242ddf1c1ed5c182cd0be7c2b7d8a23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757658"
---
# <span data-ttu-id="ae6f1-101">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ae6f1-101">New-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="ae6f1-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ae6f1-102">SYNOPSIS</span></span>
<span data-ttu-id="ae6f1-103">Skapar ett nytt rot certifikat för en VPN-klient.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-103">Creates a new VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae6f1-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ae6f1-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae6f1-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ae6f1-105">DESCRIPTION</span></span>
<span data-ttu-id="ae6f1-106">Cmdleten **New-AzureRmVpnClientRootCertificate** skapar ett nytt VPN-rotcertifikat för användning på en virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-106">The **New-AzureRmVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="ae6f1-107">Rot certifikat är 509 certifikat som identifierar rot certifikat utfärdaren: alla andra certifikat som används på gatewayen har rot certifikatet.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="ae6f1-108">Denna cmdlet skapar ett fristående certifikat som inte är kopplat till en virtuell gateway.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="ae6f1-109">I stället används certifikatet som skapas av **New-AzureRmVpnClientRootCertificate** tillsammans med New-AzureRmVirtualNetworkGateway cmdlet när du skapar en ny Gateway.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-109">Instead, the certificate created by **New-AzureRmVpnClientRootCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="ae6f1-110">Anta till exempel att du skapar ett nytt certifikat och lagrar det i en variabel som heter $Certificate.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="ae6f1-111">Du kan sedan använda detta certifikat objekt när du skapar en ny virtuell gateway.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="ae6f1-112">Till exempel:</span><span class="sxs-lookup"><span data-stu-id="ae6f1-112">For instance,</span></span>

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`

<span data-ttu-id="ae6f1-113">Mer information finns i dokumentationen för New-AzureRmVirtualNetworkGateway-cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="ae6f1-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ae6f1-114">EXAMPLES</span></span>

### <span data-ttu-id="ae6f1-115">Exempel 1: skapa aclient rot certifikat</span><span class="sxs-lookup"><span data-stu-id="ae6f1-115">Example 1: Create aclient root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="ae6f1-116">I det här exemplet skapas ett klient rot certifikat och ett certifikat objekt sparas i en variabel som heter $Certificate.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="ae6f1-117">Denna variabel kan sedan användas av **New-AzureRmVirtualNetworkGateway-** cmdleten för att lägga till ett rot certifikat till en ny virtuell nätverksgateway.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>

<span data-ttu-id="ae6f1-118">I det första kommandot används cmdleten **Get-Content** för att få en tidigare exporterad text representation av rot certifikatet. att text data lagras i en variabel som heter $Text.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>

<span data-ttu-id="ae6f1-119">Det andra kommandot använder sedan en for-slinga för att extrahera all text förutom den första raden och den sista raden, och sedan spara den extraherade texten i en variabel som heter $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>

<span data-ttu-id="ae6f1-120">I det tredje kommandot används cmdleten **New-AzureRmVpnClientRootCertificate** för att skapa certifikatet, vilket sparar det skapade objektet i en variabel som heter $Certificate.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-120">The third command uses the **New-AzureRmVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="ae6f1-121">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ae6f1-121">PARAMETERS</span></span>

### <span data-ttu-id="ae6f1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae6f1-122">-DefaultProfile</span></span>
<span data-ttu-id="ae6f1-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae6f1-124">-Namn</span><span class="sxs-lookup"><span data-stu-id="ae6f1-124">-Name</span></span>
<span data-ttu-id="ae6f1-125">Anger ett namn för det nya klient rot certifikatet.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-125">Specifies a name for the new client root certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae6f1-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="ae6f1-126">-PublicCertData</span></span>
<span data-ttu-id="ae6f1-127">Anger en text representation av rot certifikatet som ska läggas till.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="ae6f1-128">För att få text presentationen exporterar du certifikatet i CER-format (med base64-kodning) och öppnar sedan den resulterande filen i en text redigerare.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="ae6f1-129">Utdata ser ut ungefär så här (Observera att den faktiska utmatningen innehåller många fler text rader än det förkortade provet här):</span><span class="sxs-lookup"><span data-stu-id="ae6f1-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="ae6f1-130">-----Starta certifikat----------avsluta certifikat-----</span><span class="sxs-lookup"><span data-stu-id="ae6f1-130">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="ae6f1-131">PublicCertData består av alla rader mellan den första raden (-----BEGIN CERTIFICATe-----) och den sista raden (-----slut certifikatet-----) i filen.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-131">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="ae6f1-132">Du kan hämta PublicCertData genom att använda Windows PowerShell-kommandon som det här:</span><span class="sxs-lookup"><span data-stu-id="ae6f1-132">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this:</span></span>

<span data-ttu-id="ae6f1-133">$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = för ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="ae6f1-133">$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="ae6f1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae6f1-134">CommonParameters</span></span>
<span data-ttu-id="ae6f1-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae6f1-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae6f1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae6f1-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ae6f1-137">INPUTS</span></span>

###  
<span data-ttu-id="ae6f1-138">Denna cmdlet accepterar inte förloppet.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-138">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="ae6f1-139">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ae6f1-139">OUTPUTS</span></span>

###  
<span data-ttu-id="ae6f1-140">Denna cmdlet skapar nya instanser av **Microsoft. Azure. commands. Network. Models. PSVpnClientRootCertificate** -objektet.</span><span class="sxs-lookup"><span data-stu-id="ae6f1-140">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="ae6f1-141">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ae6f1-141">NOTES</span></span>

## <span data-ttu-id="ae6f1-142">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ae6f1-142">RELATED LINKS</span></span>

[<span data-ttu-id="ae6f1-143">Add-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ae6f1-143">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="ae6f1-144">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ae6f1-144">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="ae6f1-145">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="ae6f1-145">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


