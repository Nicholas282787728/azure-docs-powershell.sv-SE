---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappsslbinding
schema: 2.0.0
ms.openlocfilehash: 0a396b93a0ce1435302b1ee2f81d8700ec10a60d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93931102"
---
# <span data-ttu-id="baa5b-101">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="baa5b-101">New-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="baa5b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="baa5b-102">SYNOPSIS</span></span>
<span data-ttu-id="baa5b-103">Skapar en SSL-certifikatfil för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="baa5b-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="baa5b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="baa5b-104">SYNTAX</span></span>

### <span data-ttu-id="baa5b-105">S</span><span class="sxs-lookup"><span data-stu-id="baa5b-105">S1</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="baa5b-106">S2</span><span class="sxs-lookup"><span data-stu-id="baa5b-106">S2</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="baa5b-107">S3</span><span class="sxs-lookup"><span data-stu-id="baa5b-107">S3</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="baa5b-108">S4</span><span class="sxs-lookup"><span data-stu-id="baa5b-108">S4</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baa5b-109">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="baa5b-109">DESCRIPTION</span></span>
<span data-ttu-id="baa5b-110">Cmdleten **New-AzureRmWebAppSSLBinding** skapar ett SSL-certifikat (Secure Socket Layer) för en Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="baa5b-110">The **New-AzureRmWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="baa5b-111">Cmdleten skapar en SSL-bindning på två sätt:</span><span class="sxs-lookup"><span data-stu-id="baa5b-111">The cmdlet creates an SSL binding in two ways:</span></span> 

- <span data-ttu-id="baa5b-112">Du kan binda ett webb program till ett befintligt certifikat.</span><span class="sxs-lookup"><span data-stu-id="baa5b-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="baa5b-113">Du kan ladda upp ett nytt certifikat och sedan binda det till det nya certifikatet.</span><span class="sxs-lookup"><span data-stu-id="baa5b-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>

<span data-ttu-id="baa5b-114">Oavsett vilken metod du använder måste certifikatet och webb programmet vara associerat med samma Azure Resource Group.</span><span class="sxs-lookup"><span data-stu-id="baa5b-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="baa5b-115">Om du har ett webb program i resurs grupp A och du vill binda det webb programmet till ett certifikat i resurs grupp B är det enda sättet att göra det till att ladda upp en kopia av certifikatet till resurs gruppen A.</span><span class="sxs-lookup"><span data-stu-id="baa5b-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A.</span></span>

<span data-ttu-id="baa5b-116">Om du laddar upp ett nytt certifikat bör du tänka på följande krav för ett Azure SSL-certifikat:</span><span class="sxs-lookup"><span data-stu-id="baa5b-116">If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 

- <span data-ttu-id="baa5b-117">Certifikatet måste innehålla en privat.</span><span class="sxs-lookup"><span data-stu-id="baa5b-117">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="baa5b-118">Certifikatet måste ha formatet PFX (personal information Exchange).</span><span class="sxs-lookup"><span data-stu-id="baa5b-118">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="baa5b-119">Certifikatets subjekt namn måste stämma överens med den domän som används för att komma åt webb programmet.</span><span class="sxs-lookup"><span data-stu-id="baa5b-119">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="baa5b-120">Certifikatet måste innehålla minst 2048-bitars kryptering.</span><span class="sxs-lookup"><span data-stu-id="baa5b-120">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="baa5b-121">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="baa5b-121">EXAMPLES</span></span>

### <span data-ttu-id="baa5b-122">Exempel 1: binda ett certifikat till ett webb program</span><span class="sxs-lookup"><span data-stu-id="baa5b-122">Example 1: Bind a certificate to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="baa5b-123">Det här kommandot binder ett befintligt Azure-certifikat (ett certifikat med tumavtrycket E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) till webb programmet som heter ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="baa5b-123">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

## <span data-ttu-id="baa5b-124">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="baa5b-124">PARAMETERS</span></span>

### <span data-ttu-id="baa5b-125">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="baa5b-125">-CertificateFilePath</span></span>
<span data-ttu-id="baa5b-126">Anger sökvägen för det certifikat som ska laddas upp.</span><span class="sxs-lookup"><span data-stu-id="baa5b-126">Specifies the file path for the certificate to be uploaded.</span></span>

<span data-ttu-id="baa5b-127">Parametern *CertificateFilePath* krävs bara om certifikatet inte ännu har laddats upp till Azure.</span><span class="sxs-lookup"><span data-stu-id="baa5b-127">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa5b-128">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="baa5b-128">-CertificatePassword</span></span>
<span data-ttu-id="baa5b-129">Anger krypterings lösen ordet för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="baa5b-129">Specifies the decryption password for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa5b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baa5b-130">-DefaultProfile</span></span>
<span data-ttu-id="baa5b-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="baa5b-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baa5b-132">-Namn</span><span class="sxs-lookup"><span data-stu-id="baa5b-132">-Name</span></span>
<span data-ttu-id="baa5b-133">Anger namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="baa5b-133">Specifies the name of the Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa5b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baa5b-134">-ResourceGroupName</span></span>
<span data-ttu-id="baa5b-135">Anger namnet på resurs gruppen som certifikatet har tilldelats till.</span><span class="sxs-lookup"><span data-stu-id="baa5b-135">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="baa5b-136">Du kan inte använda parametern *ResourceGroupName* och *webapp* -parametern i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="baa5b-136">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa5b-137">-Plats</span><span class="sxs-lookup"><span data-stu-id="baa5b-137">-Slot</span></span>
<span data-ttu-id="baa5b-138">Anger namnet på webb programmets distributions plats.</span><span class="sxs-lookup"><span data-stu-id="baa5b-138">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="baa5b-139">Du kan använda Get-AzureRMWebAppSlot cmdlet för att få en kort plats.</span><span class="sxs-lookup"><span data-stu-id="baa5b-139">You can use the Get-AzureRMWebAppSlot cmdlet to get a slot.</span></span>

<span data-ttu-id="baa5b-140">Distributions platser är ett sätt för dig att mellanlagra och validera webb program utan att programmen är tillgängliga via Internet.</span><span class="sxs-lookup"><span data-stu-id="baa5b-140">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="baa5b-141">Vanligt vis distribuerar du dina ändringar på en mellanlagringsdatabas, validerar dessa ändringar och sedan distribuerar till produktions webbplatsen (Internet-tillgänglig).</span><span class="sxs-lookup"><span data-stu-id="baa5b-141">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa5b-142">-SslState</span><span class="sxs-lookup"><span data-stu-id="baa5b-142">-SslState</span></span>
<span data-ttu-id="baa5b-143">Anger om certifikatet är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="baa5b-143">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="baa5b-144">Ställ in parametern *SSLState* på 1 för att aktivera certifikatet, eller ange värdet 0 för *SSLState* om du vill inaktivera certifikatet.</span><span class="sxs-lookup"><span data-stu-id="baa5b-144">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

```yaml
Type: SslState
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa5b-145">-Tumavtryck</span><span class="sxs-lookup"><span data-stu-id="baa5b-145">-Thumbprint</span></span>
<span data-ttu-id="baa5b-146">Anger det unika ID: t för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="baa5b-146">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: S2, S4
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa5b-147">-WebApp</span><span class="sxs-lookup"><span data-stu-id="baa5b-147">-WebApp</span></span>
<span data-ttu-id="baa5b-148">Anger ett webb program.</span><span class="sxs-lookup"><span data-stu-id="baa5b-148">Specifies a Web App.</span></span>
<span data-ttu-id="baa5b-149">Om du vill hämta en webbapp använder du Get-AzureRmWebApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="baa5b-149">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

<span data-ttu-id="baa5b-150">Du kan inte använda *webapp* -parametern i samma kommando som parametern *ResourceGroupName* och/eller *WebAppName*.</span><span class="sxs-lookup"><span data-stu-id="baa5b-150">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Site
Parameter Sets: S3, S4
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="baa5b-151">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="baa5b-151">-WebAppName</span></span>
<span data-ttu-id="baa5b-152">Anger namnet på den webbapp som den nya SSL-bindningen skapas för.</span><span class="sxs-lookup"><span data-stu-id="baa5b-152">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>

<span data-ttu-id="baa5b-153">Du kan inte använda parametern *WebAppName* och *webapp* -parametern i samma kommando.</span><span class="sxs-lookup"><span data-stu-id="baa5b-153">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baa5b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa5b-154">CommonParameters</span></span>
<span data-ttu-id="baa5b-155">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baa5b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa5b-156">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baa5b-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa5b-157">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="baa5b-157">INPUTS</span></span>

### <span data-ttu-id="baa5b-158">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="baa5b-158">Site</span></span>
<span data-ttu-id="baa5b-159">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="baa5b-159">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="baa5b-160">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="baa5b-160">OUTPUTS</span></span>

## <span data-ttu-id="baa5b-161">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="baa5b-161">NOTES</span></span>

## <span data-ttu-id="baa5b-162">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="baa5b-162">RELATED LINKS</span></span>

[<span data-ttu-id="baa5b-163">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="baa5b-163">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="baa5b-164">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="baa5b-164">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="baa5b-165">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="baa5b-165">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="baa5b-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="baa5b-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


