---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 1b1f16c8d48debb04ad1f38c03aa58e65f9953a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577278"
---
# <span data-ttu-id="0678f-101">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="0678f-101">Set-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="0678f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="0678f-102">SYNOPSIS</span></span>
<span data-ttu-id="0678f-103">Ändrar ett API-Management-certifikat som är konfigurerat för ömsesidig autentisering med Server delen.</span><span class="sxs-lookup"><span data-stu-id="0678f-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0678f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="0678f-104">SYNTAX</span></span>

### <span data-ttu-id="0678f-105">LoadFromFile (standard)</span><span class="sxs-lookup"><span data-stu-id="0678f-105">LoadFromFile (Default)</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0678f-106">RAW</span><span class="sxs-lookup"><span data-stu-id="0678f-106">Raw</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0678f-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="0678f-107">DESCRIPTION</span></span>
<span data-ttu-id="0678f-108">Cmdleten **set-AzureRmApiManagementCertificate** ändrar ett certifikat för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="0678f-108">The **Set-AzureRmApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="0678f-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="0678f-109">EXAMPLES</span></span>

### <span data-ttu-id="0678f-110">Exempel 1: ändra ett certifikat</span><span class="sxs-lookup"><span data-stu-id="0678f-110">Example 1: Modify a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="0678f-111">Det här kommandot ändrar angivet API-Management-certifikat.</span><span class="sxs-lookup"><span data-stu-id="0678f-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="0678f-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="0678f-112">PARAMETERS</span></span>

### <span data-ttu-id="0678f-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="0678f-113">-CertificateId</span></span>
<span data-ttu-id="0678f-114">Anger ID för det certifikat som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="0678f-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="0678f-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="0678f-115">-Context</span></span>
<span data-ttu-id="0678f-116">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="0678f-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0678f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0678f-117">-DefaultProfile</span></span>
<span data-ttu-id="0678f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="0678f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="0678f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0678f-119">-PassThru</span></span>
<span data-ttu-id="0678f-120">passthru</span><span class="sxs-lookup"><span data-stu-id="0678f-120">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0678f-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="0678f-121">-PfxBytes</span></span>
<span data-ttu-id="0678f-122">Anger en matris med byte för certifikat filen i PFX-format.</span><span class="sxs-lookup"><span data-stu-id="0678f-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="0678f-123">Den här parametern är obligatorisk om du inte anger parametern *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="0678f-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: Byte[]
Parameter Sets: Raw
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0678f-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="0678f-124">-PfxFilePath</span></span>
<span data-ttu-id="0678f-125">Anger sökvägen till certifikat filen i PFX-format för att skapa och ladda upp.</span><span class="sxs-lookup"><span data-stu-id="0678f-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="0678f-126">Den här parametern är obligatorisk om du inte anger parametern *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="0678f-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: LoadFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0678f-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="0678f-127">-PfxPassword</span></span>
<span data-ttu-id="0678f-128">Anger lösen ordet för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="0678f-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="0678f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0678f-129">CommonParameters</span></span>
<span data-ttu-id="0678f-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0678f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0678f-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0678f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0678f-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="0678f-132">INPUTS</span></span>

### <span data-ttu-id="0678f-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="0678f-133">None</span></span>
<span data-ttu-id="0678f-134">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="0678f-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0678f-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="0678f-135">OUTPUTS</span></span>

### <span data-ttu-id="0678f-136">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="0678f-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="0678f-137">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="0678f-137">NOTES</span></span>

## <span data-ttu-id="0678f-138">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="0678f-138">RELATED LINKS</span></span>

[<span data-ttu-id="0678f-139">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="0678f-139">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="0678f-140">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="0678f-140">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="0678f-141">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="0678f-141">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)


