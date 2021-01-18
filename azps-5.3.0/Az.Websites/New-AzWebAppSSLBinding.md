---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 2fff18033febbab23083127628959d2fca9305a3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98522098"
---
# <span data-ttu-id="c0f16-101">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="c0f16-101">New-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="c0f16-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c0f16-102">SYNOPSIS</span></span>
<span data-ttu-id="c0f16-103">Skapar en SSL-certifikatfil för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c0f16-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

## <span data-ttu-id="c0f16-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c0f16-104">SYNTAX</span></span>

### <span data-ttu-id="c0f16-105">S</span><span class="sxs-lookup"><span data-stu-id="c0f16-105">S1</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c0f16-106">S2</span><span class="sxs-lookup"><span data-stu-id="c0f16-106">S2</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0f16-107">S3</span><span class="sxs-lookup"><span data-stu-id="c0f16-107">S3</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0f16-108">S4</span><span class="sxs-lookup"><span data-stu-id="c0f16-108">S4</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0f16-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c0f16-109">DESCRIPTION</span></span>
<span data-ttu-id="c0f16-110">Cmdleten **New-AzWebAppSSLBinding** skapar ett SSL-certifikat (Secure Socket Layer) för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c0f16-110">The **New-AzWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="c0f16-111">Cmdleten skapar en SSL-bindning på två sätt:</span><span class="sxs-lookup"><span data-stu-id="c0f16-111">The cmdlet creates an SSL binding in two ways:</span></span> 
- <span data-ttu-id="c0f16-112">Du kan binda ett webb program till ett befintligt certifikat.</span><span class="sxs-lookup"><span data-stu-id="c0f16-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="c0f16-113">Du kan ladda upp ett nytt certifikat och sedan binda det till det nya certifikatet.</span><span class="sxs-lookup"><span data-stu-id="c0f16-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>
<span data-ttu-id="c0f16-114">Oavsett vilken metod du använder måste certifikatet och webb programmet vara associerat med samma Azure Resource Group.</span><span class="sxs-lookup"><span data-stu-id="c0f16-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="c0f16-115">Om du har ett webb program i resurs grupp A och du vill binda det webb programmet till ett certifikat i resurs grupp B är det enda sättet att göra det till att ladda upp en kopia av certifikatet till resurs gruppen A. Om du laddar upp ett nytt certifikat bör du tänka på följande krav för ett Azure SSL-certifikat:</span><span class="sxs-lookup"><span data-stu-id="c0f16-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A. If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 
- <span data-ttu-id="c0f16-116">Certifikatet måste innehålla en privat.</span><span class="sxs-lookup"><span data-stu-id="c0f16-116">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="c0f16-117">Certifikatet måste ha formatet PFX (personal information Exchange).</span><span class="sxs-lookup"><span data-stu-id="c0f16-117">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="c0f16-118">Certifikatets subjekt namn måste stämma överens med den domän som används för att komma åt webb programmet.</span><span class="sxs-lookup"><span data-stu-id="c0f16-118">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="c0f16-119">Certifikatet måste innehålla minst 2048-bitars kryptering.</span><span class="sxs-lookup"><span data-stu-id="c0f16-119">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="c0f16-120">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c0f16-120">EXAMPLES</span></span>

### <span data-ttu-id="c0f16-121">Exempel 1: binda ett certifikat till ett webb program</span><span class="sxs-lookup"><span data-stu-id="c0f16-121">Example 1: Bind a certificate to a Web App</span></span>
```powershell
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="c0f16-122">Det här kommandot binder ett befintligt Azure-certifikat (ett certifikat med tumavtrycket E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) till webb programmet som heter ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="c0f16-122">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

### <span data-ttu-id="c0f16-123">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="c0f16-123">Example 2</span></span>

<span data-ttu-id="c0f16-124">Skapar en SSL-certifikatfil för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c0f16-124">Creates an SSL certificate binding for an Azure Web App.</span></span> <span data-ttu-id="c0f16-125">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="c0f16-125">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppSSLBinding -Name 'www.contoso.com' -ResourceGroupName 'ContosoResourceGroup' -SslState Disabled -Thumbprint 'E3A38EBA60CAA1C162785A2E1C44A15AD450199C3' -WebAppName 'ContosoWebApp'
```

## <span data-ttu-id="c0f16-126">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c0f16-126">PARAMETERS</span></span>

### <span data-ttu-id="c0f16-127">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="c0f16-127">-CertificateFilePath</span></span>
<span data-ttu-id="c0f16-128">Anger sökvägen för det certifikat som ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="c0f16-128">Specifies the file path for the certificate to be uploaded.</span></span>
<span data-ttu-id="c0f16-129">Parametern *CertificateFilePath* krävs bara om certifikatet inte ännu har laddats upp till Azure.</span><span class="sxs-lookup"><span data-stu-id="c0f16-129">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

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

### <span data-ttu-id="c0f16-130">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c0f16-130">-CertificatePassword</span></span>
<span data-ttu-id="c0f16-131">Anger krypterings lösen ordet för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="c0f16-131">Specifies the decryption password for the certificate.</span></span>

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

### <span data-ttu-id="c0f16-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0f16-132">-DefaultProfile</span></span>
<span data-ttu-id="c0f16-133">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c0f16-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0f16-134">-Namn</span><span class="sxs-lookup"><span data-stu-id="c0f16-134">-Name</span></span>
<span data-ttu-id="c0f16-135">Anger namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="c0f16-135">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="c0f16-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0f16-136">-ResourceGroupName</span></span>
<span data-ttu-id="c0f16-137">Anger namnet på resurs gruppen som certifikatet har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="c0f16-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="c0f16-138">Du kan inte använda parametern *ResourceGroupName* och *webapp* -parametern i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="c0f16-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="c0f16-139">-Plats</span><span class="sxs-lookup"><span data-stu-id="c0f16-139">-Slot</span></span>
<span data-ttu-id="c0f16-140">Anger namnet på webb programmets distributions plats.</span><span class="sxs-lookup"><span data-stu-id="c0f16-140">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="c0f16-141">Du kan använda Get-AzWebAppSlot cmdlet för att få en kort plats.</span><span class="sxs-lookup"><span data-stu-id="c0f16-141">You can use the Get-AzWebAppSlot cmdlet to get a slot.</span></span>
<span data-ttu-id="c0f16-142">Distributions platser är ett sätt för dig att mellanlagra och validera webb program utan att programmen är tillgängliga via Internet.</span><span class="sxs-lookup"><span data-stu-id="c0f16-142">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="c0f16-143">Vanligt vis distribuerar du dina ändringar på en mellanlagringsdatabas, validerar dessa ändringar och sedan distribuerar till produktions webbplatsen (Internet-tillgänglig).</span><span class="sxs-lookup"><span data-stu-id="c0f16-143">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

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

### <span data-ttu-id="c0f16-144">-SslState</span><span class="sxs-lookup"><span data-stu-id="c0f16-144">-SslState</span></span>
<span data-ttu-id="c0f16-145">Anger om certifikatet är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="c0f16-145">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="c0f16-146">Ställ in parametern *SSLState* på 1 för att aktivera certifikatet, eller ange värdet 0 för *SSLState* om du vill inaktivera certifikatet.</span><span class="sxs-lookup"><span data-stu-id="c0f16-146">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

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

### <span data-ttu-id="c0f16-147">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="c0f16-147">-Thumbprint</span></span>
<span data-ttu-id="c0f16-148">Anger det unika ID: t för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="c0f16-148">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="c0f16-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c0f16-149">-WebApp</span></span>
<span data-ttu-id="c0f16-150">Anger ett webb program.</span><span class="sxs-lookup"><span data-stu-id="c0f16-150">Specifies a Web App.</span></span>
<span data-ttu-id="c0f16-151">Om du vill hämta en webbapp använder du Get-AzWebApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0f16-151">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="c0f16-152">Du kan inte använda *webapp* -parametern i samma kommando som parametern *ResourceGroupName* och/eller *WebAppName*.</span><span class="sxs-lookup"><span data-stu-id="c0f16-152">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

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

### <span data-ttu-id="c0f16-153">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="c0f16-153">-WebAppName</span></span>
<span data-ttu-id="c0f16-154">Anger namnet på den webbapp som den nya SSL-bindningen skapas för.</span><span class="sxs-lookup"><span data-stu-id="c0f16-154">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>
<span data-ttu-id="c0f16-155">Du kan inte använda parametern *WebAppName* och *webapp* -parametern i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="c0f16-155">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="c0f16-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0f16-156">CommonParameters</span></span>
<span data-ttu-id="c0f16-157">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0f16-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0f16-158">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0f16-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0f16-159">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c0f16-159">INPUTS</span></span>

### <span data-ttu-id="c0f16-160">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="c0f16-160">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c0f16-161">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c0f16-161">OUTPUTS</span></span>

### <span data-ttu-id="c0f16-162">Microsoft. Azure. Management. webbplatser. Models. HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="c0f16-162">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="c0f16-163">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c0f16-163">NOTES</span></span>

## <span data-ttu-id="c0f16-164">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c0f16-164">RELATED LINKS</span></span>

[<span data-ttu-id="c0f16-165">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="c0f16-165">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="c0f16-166">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="c0f16-166">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="c0f16-167">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="c0f16-167">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="c0f16-168">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c0f16-168">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


