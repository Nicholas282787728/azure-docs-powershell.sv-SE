---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 55b95cec3e699872688fad5daeb0d2f7e89059c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578636"
---
# <span data-ttu-id="b1848-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b1848-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="b1848-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="b1848-102">SYNOPSIS</span></span>
<span data-ttu-id="b1848-103">Skapar ett API-Management-certifikat som används vid autentisering med Server delen.</span><span class="sxs-lookup"><span data-stu-id="b1848-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1848-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="b1848-104">SYNTAX</span></span>

### <span data-ttu-id="b1848-105">Ladda från fil (standard)</span><span class="sxs-lookup"><span data-stu-id="b1848-105">Load from file (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1848-106">RAW</span><span class="sxs-lookup"><span data-stu-id="b1848-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1848-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="b1848-107">DESCRIPTION</span></span>
<span data-ttu-id="b1848-108">Cmdleten **New-AzureRmApiManagementCertificate** skapar ett Azure API Management-certifikat.</span><span class="sxs-lookup"><span data-stu-id="b1848-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="b1848-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="b1848-109">EXAMPLES</span></span>

### <span data-ttu-id="b1848-110">Exempel 1: skapa och ladda upp ett certifikat</span><span class="sxs-lookup"><span data-stu-id="b1848-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="b1848-111">Det här kommandot skapar ett API-Management-certifikat och laddar upp det.</span><span class="sxs-lookup"><span data-stu-id="b1848-111">This command creates an API Management certificate and uploads it.</span></span>

## <span data-ttu-id="b1848-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="b1848-112">PARAMETERS</span></span>

### <span data-ttu-id="b1848-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="b1848-113">-CertificateId</span></span>
<span data-ttu-id="b1848-114">Anger ID för det certifikat som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="b1848-114">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="b1848-115">Om du inte anger den här parametern genereras ett ID för dig.</span><span class="sxs-lookup"><span data-stu-id="b1848-115">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1848-116">-Kontext</span><span class="sxs-lookup"><span data-stu-id="b1848-116">-Context</span></span>
<span data-ttu-id="b1848-117">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="b1848-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b1848-118">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="b1848-118">-PfxBytes</span></span>
<span data-ttu-id="b1848-119">Anger en matris med byte för certifikat filen i PFX-format.</span><span class="sxs-lookup"><span data-stu-id="b1848-119">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="b1848-120">Den här parametern är obligatorisk om du inte anger parametern *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="b1848-120">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="b1848-121">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="b1848-121">-PfxFilePath</span></span>
<span data-ttu-id="b1848-122">Anger sökvägen till certifikat filen i PFX-format för att skapa och ladda upp.</span><span class="sxs-lookup"><span data-stu-id="b1848-122">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="b1848-123">Den här parametern är obligatorisk om du inte anger parametern *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="b1848-123">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Load from file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1848-124">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="b1848-124">-PfxPassword</span></span>
<span data-ttu-id="b1848-125">Anger lösen ordet för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="b1848-125">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="b1848-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1848-126">-DefaultProfile</span></span>
<span data-ttu-id="b1848-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="b1848-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1848-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1848-128">CommonParameters</span></span>
<span data-ttu-id="b1848-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1848-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1848-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1848-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1848-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="b1848-131">INPUTS</span></span>

## <span data-ttu-id="b1848-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="b1848-132">OUTPUTS</span></span>

### <span data-ttu-id="b1848-133">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b1848-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="b1848-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="b1848-134">NOTES</span></span>

## <span data-ttu-id="b1848-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="b1848-135">RELATED LINKS</span></span>

[<span data-ttu-id="b1848-136">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b1848-136">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="b1848-137">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b1848-137">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="b1848-138">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="b1848-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


