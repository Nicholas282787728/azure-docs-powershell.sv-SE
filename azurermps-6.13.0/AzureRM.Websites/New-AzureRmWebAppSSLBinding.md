---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 33efe02dd463334745e39d846d0b43c2ccd9dd6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757320"
---
# <span data-ttu-id="ad204-101">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="ad204-101">New-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="ad204-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ad204-102">SYNOPSIS</span></span>
<span data-ttu-id="ad204-103">Skapar en SSL-certifikatfil för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ad204-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad204-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ad204-104">SYNTAX</span></span>

### <span data-ttu-id="ad204-105">S</span><span class="sxs-lookup"><span data-stu-id="ad204-105">S1</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad204-106">S2</span><span class="sxs-lookup"><span data-stu-id="ad204-106">S2</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad204-107">S3</span><span class="sxs-lookup"><span data-stu-id="ad204-107">S3</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad204-108">S4</span><span class="sxs-lookup"><span data-stu-id="ad204-108">S4</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad204-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ad204-109">DESCRIPTION</span></span>
<span data-ttu-id="ad204-110">Cmdleten **New-AzureRmWebAppSSLBinding** skapar ett SSL-certifikat (Secure Socket Layer) för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="ad204-110">The **New-AzureRmWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="ad204-111">Cmdleten skapar en SSL-bindning på två sätt:</span><span class="sxs-lookup"><span data-stu-id="ad204-111">The cmdlet creates an SSL binding in two ways:</span></span> 
- <span data-ttu-id="ad204-112">Du kan binda ett webb program till ett befintligt certifikat.</span><span class="sxs-lookup"><span data-stu-id="ad204-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="ad204-113">Du kan ladda upp ett nytt certifikat och sedan binda det till det nya certifikatet.</span><span class="sxs-lookup"><span data-stu-id="ad204-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>
<span data-ttu-id="ad204-114">Oavsett vilken metod du använder måste certifikatet och webb programmet vara associerat med samma Azure Resource Group.</span><span class="sxs-lookup"><span data-stu-id="ad204-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="ad204-115">Om du har ett webb program i resurs grupp A och du vill binda det webb programmet till ett certifikat i resurs grupp B är det enda sättet att göra det till att ladda upp en kopia av certifikatet till resurs gruppen A. Om du laddar upp ett nytt certifikat bör du tänka på följande krav för ett Azure SSL-certifikat:</span><span class="sxs-lookup"><span data-stu-id="ad204-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A. If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 
- <span data-ttu-id="ad204-116">Certifikatet måste innehålla en privat.</span><span class="sxs-lookup"><span data-stu-id="ad204-116">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="ad204-117">Certifikatet måste ha formatet PFX (personal information Exchange).</span><span class="sxs-lookup"><span data-stu-id="ad204-117">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="ad204-118">Certifikatets subjekt namn måste stämma överens med den domän som används för att komma åt webb programmet.</span><span class="sxs-lookup"><span data-stu-id="ad204-118">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="ad204-119">Certifikatet måste innehålla minst 2048-bitars kryptering.</span><span class="sxs-lookup"><span data-stu-id="ad204-119">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="ad204-120">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ad204-120">EXAMPLES</span></span>

### <span data-ttu-id="ad204-121">Exempel 1: binda ett certifikat till ett webb program</span><span class="sxs-lookup"><span data-stu-id="ad204-121">Example 1: Bind a certificate to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="ad204-122">Det här kommandot binder ett befintligt Azure-certifikat (ett certifikat med tumavtrycket E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) till webb programmet som heter ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="ad204-122">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

## <span data-ttu-id="ad204-123">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ad204-123">PARAMETERS</span></span>

### <span data-ttu-id="ad204-124">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="ad204-124">-CertificateFilePath</span></span>
<span data-ttu-id="ad204-125">Anger sökvägen för det certifikat som ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="ad204-125">Specifies the file path for the certificate to be uploaded.</span></span>
<span data-ttu-id="ad204-126">Parametern *CertificateFilePath* krävs bara om certifikatet inte ännu har laddats upp till Azure.</span><span class="sxs-lookup"><span data-stu-id="ad204-126">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad204-127">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="ad204-127">-CertificatePassword</span></span>
<span data-ttu-id="ad204-128">Anger krypterings lösen ordet för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="ad204-128">Specifies the decryption password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad204-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad204-129">-DefaultProfile</span></span>
<span data-ttu-id="ad204-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ad204-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad204-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="ad204-131">-Name</span></span>
<span data-ttu-id="ad204-132">Anger namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="ad204-132">Specifies the name of the Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad204-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad204-133">-ResourceGroupName</span></span>
<span data-ttu-id="ad204-134">Anger namnet på resurs gruppen som certifikatet har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="ad204-134">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="ad204-135">Du kan inte använda parametern *ResourceGroupName* och *webapp* -parametern i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="ad204-135">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad204-136">-Plats</span><span class="sxs-lookup"><span data-stu-id="ad204-136">-Slot</span></span>
<span data-ttu-id="ad204-137">Anger namnet på webb programmets distributions plats.</span><span class="sxs-lookup"><span data-stu-id="ad204-137">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="ad204-138">Du kan använda Get-AzureRMWebAppSlot cmdlet för att få en kort plats.</span><span class="sxs-lookup"><span data-stu-id="ad204-138">You can use the Get-AzureRMWebAppSlot cmdlet to get a slot.</span></span>
<span data-ttu-id="ad204-139">Distributions platser är ett sätt för dig att mellanlagra och validera webb program utan att programmen är tillgängliga via Internet.</span><span class="sxs-lookup"><span data-stu-id="ad204-139">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="ad204-140">Vanligt vis distribuerar du dina ändringar på en mellanlagringsdatabas, validerar dessa ändringar och sedan distribuerar till produktions webbplatsen (Internet-tillgänglig).</span><span class="sxs-lookup"><span data-stu-id="ad204-140">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad204-141">-SslState</span><span class="sxs-lookup"><span data-stu-id="ad204-141">-SslState</span></span>
<span data-ttu-id="ad204-142">Anger om certifikatet är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="ad204-142">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="ad204-143">Ställ in parametern *SSLState* på 1 för att aktivera certifikatet, eller ange värdet 0 för *SSLState* om du vill inaktivera certifikatet.</span><span class="sxs-lookup"><span data-stu-id="ad204-143">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.WebSites.Models.SslState]
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad204-144">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="ad204-144">-Thumbprint</span></span>
<span data-ttu-id="ad204-145">Anger det unika ID: t för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="ad204-145">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S2, S4
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad204-146">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ad204-146">-WebApp</span></span>
<span data-ttu-id="ad204-147">Anger ett webb program.</span><span class="sxs-lookup"><span data-stu-id="ad204-147">Specifies a Web App.</span></span>
<span data-ttu-id="ad204-148">Om du vill hämta en webbapp använder du Get-AzureRmWebApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad204-148">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>
<span data-ttu-id="ad204-149">Du kan inte använda *webapp* -parametern i samma kommando som parametern *ResourceGroupName* och/eller *WebAppName*.</span><span class="sxs-lookup"><span data-stu-id="ad204-149">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S3, S4
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad204-150">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="ad204-150">-WebAppName</span></span>
<span data-ttu-id="ad204-151">Anger namnet på den webbapp som den nya SSL-bindningen skapas för.</span><span class="sxs-lookup"><span data-stu-id="ad204-151">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>
<span data-ttu-id="ad204-152">Du kan inte använda parametern *WebAppName* och *webapp* -parametern i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="ad204-152">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad204-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad204-153">CommonParameters</span></span>
<span data-ttu-id="ad204-154">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad204-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad204-155">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad204-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad204-156">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ad204-156">INPUTS</span></span>

### <span data-ttu-id="ad204-157">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="ad204-157">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="ad204-158">Parametrar: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ad204-158">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="ad204-159">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ad204-159">OUTPUTS</span></span>

### <span data-ttu-id="ad204-160">Microsoft. Azure. Management. webbplatser. Models. HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="ad204-160">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="ad204-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ad204-161">NOTES</span></span>

## <span data-ttu-id="ad204-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ad204-162">RELATED LINKS</span></span>

[<span data-ttu-id="ad204-163">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="ad204-163">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="ad204-164">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="ad204-164">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="ad204-165">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="ad204-165">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="ad204-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ad204-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


