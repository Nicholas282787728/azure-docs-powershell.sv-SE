---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCertificate.md
ms.openlocfilehash: 1fe178b80a39d4587a97207b6bd2d8cf6f4c9731
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93754904"
---
# <span data-ttu-id="c65c3-101">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="c65c3-101">New-AzApiManagementCertificate</span></span>

## <span data-ttu-id="c65c3-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c65c3-102">SYNOPSIS</span></span>
<span data-ttu-id="c65c3-103">Skapar ett API-Management-certifikat som används vid autentisering med Server delen.</span><span class="sxs-lookup"><span data-stu-id="c65c3-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

## <span data-ttu-id="c65c3-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c65c3-104">SYNTAX</span></span>

### <span data-ttu-id="c65c3-105">LoadFromFile (standard)</span><span class="sxs-lookup"><span data-stu-id="c65c3-105">LoadFromFile (Default)</span></span>
```
New-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c65c3-106">RAW</span><span class="sxs-lookup"><span data-stu-id="c65c3-106">Raw</span></span>
```
New-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>] -PfxBytes <Byte[]>
 -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c65c3-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c65c3-107">DESCRIPTION</span></span>
<span data-ttu-id="c65c3-108">Cmdleten **New-AzApiManagementCertificate** skapar ett Azure API Management-certifikat.</span><span class="sxs-lookup"><span data-stu-id="c65c3-108">The **New-AzApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="c65c3-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c65c3-109">EXAMPLES</span></span>

### <span data-ttu-id="c65c3-110">Exempel 1: skapa och ladda upp ett certifikat</span><span class="sxs-lookup"><span data-stu-id="c65c3-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="c65c3-111">Det här kommandot laddar upp ett certifikat för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="c65c3-111">This command uploads a certificate to Api Management.</span></span> <span data-ttu-id="c65c3-112">Det här certifikatet kan användas för ömsesidig autentisering med Server dels med principer.</span><span class="sxs-lookup"><span data-stu-id="c65c3-112">This certificate can be used for mutual authentication with backend using policies.</span></span>

## <span data-ttu-id="c65c3-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c65c3-113">PARAMETERS</span></span>

### <span data-ttu-id="c65c3-114">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="c65c3-114">-CertificateId</span></span>
<span data-ttu-id="c65c3-115">Anger ID för det certifikat som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="c65c3-115">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="c65c3-116">Om du inte anger den här parametern genereras ett ID för dig.</span><span class="sxs-lookup"><span data-stu-id="c65c3-116">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="c65c3-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c65c3-117">-Context</span></span>
<span data-ttu-id="c65c3-118">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c65c3-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c65c3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c65c3-119">-DefaultProfile</span></span>
<span data-ttu-id="c65c3-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c65c3-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c65c3-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="c65c3-121">-PfxBytes</span></span>
<span data-ttu-id="c65c3-122">Anger en matris med byte för certifikat filen i PFX-format.</span><span class="sxs-lookup"><span data-stu-id="c65c3-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="c65c3-123">Den här parametern är obligatorisk om du inte anger parametern *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="c65c3-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="c65c3-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="c65c3-124">-PfxFilePath</span></span>
<span data-ttu-id="c65c3-125">Anger sökvägen till certifikat filen i PFX-format för att skapa och ladda upp.</span><span class="sxs-lookup"><span data-stu-id="c65c3-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="c65c3-126">Den här parametern är obligatorisk om du inte anger parametern *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="c65c3-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="c65c3-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="c65c3-127">-PfxPassword</span></span>
<span data-ttu-id="c65c3-128">Anger lösen ordet för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="c65c3-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="c65c3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c65c3-129">CommonParameters</span></span>
<span data-ttu-id="c65c3-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c65c3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c65c3-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c65c3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c65c3-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c65c3-132">INPUTS</span></span>

### <span data-ttu-id="c65c3-133">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c65c3-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c65c3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c65c3-134">System.String</span></span>

### <span data-ttu-id="c65c3-135">System. byte []</span><span class="sxs-lookup"><span data-stu-id="c65c3-135">System.Byte[]</span></span>

## <span data-ttu-id="c65c3-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c65c3-136">OUTPUTS</span></span>

### <span data-ttu-id="c65c3-137">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="c65c3-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="c65c3-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c65c3-138">NOTES</span></span>

## <span data-ttu-id="c65c3-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c65c3-139">RELATED LINKS</span></span>

[<span data-ttu-id="c65c3-140">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="c65c3-140">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="c65c3-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="c65c3-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="c65c3-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="c65c3-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


