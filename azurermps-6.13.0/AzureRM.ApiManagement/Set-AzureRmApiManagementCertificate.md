---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: f7712a7938617d979dad2feabf4d2b2126e20433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573031"
---
# <span data-ttu-id="1da69-101">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1da69-101">Set-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="1da69-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="1da69-102">SYNOPSIS</span></span>
<span data-ttu-id="1da69-103">Ändrar ett API-Management-certifikat som är konfigurerat för ömsesidig autentisering med Server delen.</span><span class="sxs-lookup"><span data-stu-id="1da69-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1da69-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="1da69-104">SYNTAX</span></span>

### <span data-ttu-id="1da69-105">LoadFromFile (standard)</span><span class="sxs-lookup"><span data-stu-id="1da69-105">LoadFromFile (Default)</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1da69-106">RAW</span><span class="sxs-lookup"><span data-stu-id="1da69-106">Raw</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1da69-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="1da69-107">DESCRIPTION</span></span>
<span data-ttu-id="1da69-108">Cmdleten **set-AzureRmApiManagementCertificate** ändrar ett certifikat för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="1da69-108">The **Set-AzureRmApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="1da69-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="1da69-109">EXAMPLES</span></span>

### <span data-ttu-id="1da69-110">Exempel 1: ändra ett certifikat</span><span class="sxs-lookup"><span data-stu-id="1da69-110">Example 1: Modify a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="1da69-111">Det här kommandot ändrar angivet API-Management-certifikat.</span><span class="sxs-lookup"><span data-stu-id="1da69-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="1da69-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="1da69-112">PARAMETERS</span></span>

### <span data-ttu-id="1da69-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="1da69-113">-CertificateId</span></span>
<span data-ttu-id="1da69-114">Anger ID för det certifikat som ska ändras.</span><span class="sxs-lookup"><span data-stu-id="1da69-114">Specifies the ID of the certificate to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1da69-115">-Kontext</span><span class="sxs-lookup"><span data-stu-id="1da69-115">-Context</span></span>
<span data-ttu-id="1da69-116">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="1da69-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1da69-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1da69-117">-DefaultProfile</span></span>
<span data-ttu-id="1da69-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="1da69-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1da69-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1da69-119">-PassThru</span></span>
<span data-ttu-id="1da69-120">passthru</span><span class="sxs-lookup"><span data-stu-id="1da69-120">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1da69-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="1da69-121">-PfxBytes</span></span>
<span data-ttu-id="1da69-122">Anger en matris med byte för certifikat filen i PFX-format.</span><span class="sxs-lookup"><span data-stu-id="1da69-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="1da69-123">Den här parametern är obligatorisk om du inte anger parametern *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="1da69-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1da69-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="1da69-124">-PfxFilePath</span></span>
<span data-ttu-id="1da69-125">Anger sökvägen till certifikat filen i PFX-format för att skapa och ladda upp.</span><span class="sxs-lookup"><span data-stu-id="1da69-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="1da69-126">Den här parametern är obligatorisk om du inte anger parametern *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="1da69-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1da69-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="1da69-127">-PfxPassword</span></span>
<span data-ttu-id="1da69-128">Anger lösen ordet för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="1da69-128">Specifies the password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1da69-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1da69-129">CommonParameters</span></span>
<span data-ttu-id="1da69-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1da69-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1da69-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1da69-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1da69-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="1da69-132">INPUTS</span></span>

### <span data-ttu-id="1da69-133">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1da69-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1da69-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1da69-134">System.String</span></span>

### <span data-ttu-id="1da69-135">System. byte []</span><span class="sxs-lookup"><span data-stu-id="1da69-135">System.Byte[]</span></span>

### <span data-ttu-id="1da69-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1da69-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1da69-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="1da69-137">OUTPUTS</span></span>

### <span data-ttu-id="1da69-138">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1da69-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="1da69-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="1da69-139">NOTES</span></span>

## <span data-ttu-id="1da69-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="1da69-140">RELATED LINKS</span></span>

[<span data-ttu-id="1da69-141">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1da69-141">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="1da69-142">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1da69-142">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="1da69-143">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1da69-143">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)


