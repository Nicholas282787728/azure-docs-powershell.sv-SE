---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCertificate.md
ms.openlocfilehash: e2f32bc5d05121411a109c1371b52b41843cfc56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93745780"
---
# <span data-ttu-id="6d043-101">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="6d043-101">New-AzApiManagementCertificate</span></span>

## <span data-ttu-id="6d043-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6d043-102">SYNOPSIS</span></span>
<span data-ttu-id="6d043-103">Skapar ett API-Management-certifikat som används vid autentisering med Server delen.</span><span class="sxs-lookup"><span data-stu-id="6d043-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

## <span data-ttu-id="6d043-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6d043-104">SYNTAX</span></span>

### <span data-ttu-id="6d043-105">LoadFromFile (standard)</span><span class="sxs-lookup"><span data-stu-id="6d043-105">LoadFromFile (Default)</span></span>
```
New-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d043-106">RAW</span><span class="sxs-lookup"><span data-stu-id="6d043-106">Raw</span></span>
```
New-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>] -PfxBytes <Byte[]>
 -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d043-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6d043-107">DESCRIPTION</span></span>
<span data-ttu-id="6d043-108">Cmdleten **New-AzApiManagementCertificate** skapar ett Azure API Management-certifikat.</span><span class="sxs-lookup"><span data-stu-id="6d043-108">The **New-AzApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="6d043-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6d043-109">EXAMPLES</span></span>

### <span data-ttu-id="6d043-110">Exempel 1: skapa och ladda upp ett certifikat</span><span class="sxs-lookup"><span data-stu-id="6d043-110">Example 1: Create and upload a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="6d043-111">Det här kommandot laddar upp ett certifikat för API-hantering.</span><span class="sxs-lookup"><span data-stu-id="6d043-111">This command uploads a certificate to Api Management.</span></span> <span data-ttu-id="6d043-112">Det här certifikatet kan användas för ömsesidig autentisering med Server dels med principer.</span><span class="sxs-lookup"><span data-stu-id="6d043-112">This certificate can be used for mutual authentication with backend using policies.</span></span>

## <span data-ttu-id="6d043-113">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6d043-113">PARAMETERS</span></span>

### <span data-ttu-id="6d043-114">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="6d043-114">-CertificateId</span></span>
<span data-ttu-id="6d043-115">Anger ID för det certifikat som ska skapas.</span><span class="sxs-lookup"><span data-stu-id="6d043-115">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="6d043-116">Om du inte anger den här parametern genereras ett ID för dig.</span><span class="sxs-lookup"><span data-stu-id="6d043-116">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="6d043-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="6d043-117">-Context</span></span>
<span data-ttu-id="6d043-118">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="6d043-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d043-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d043-119">-DefaultProfile</span></span>
<span data-ttu-id="6d043-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="6d043-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d043-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="6d043-121">-PfxBytes</span></span>
<span data-ttu-id="6d043-122">Anger en matris med byte för certifikat filen i PFX-format.</span><span class="sxs-lookup"><span data-stu-id="6d043-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="6d043-123">Den här parametern är obligatorisk om du inte anger parametern *PfxFilePath* .</span><span class="sxs-lookup"><span data-stu-id="6d043-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="6d043-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="6d043-124">-PfxFilePath</span></span>
<span data-ttu-id="6d043-125">Anger sökvägen till certifikat filen i PFX-format för att skapa och ladda upp.</span><span class="sxs-lookup"><span data-stu-id="6d043-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="6d043-126">Den här parametern är obligatorisk om du inte anger parametern *PfxBytes* .</span><span class="sxs-lookup"><span data-stu-id="6d043-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="6d043-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="6d043-127">-PfxPassword</span></span>
<span data-ttu-id="6d043-128">Anger lösen ordet för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="6d043-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="6d043-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d043-129">CommonParameters</span></span>
<span data-ttu-id="6d043-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d043-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d043-131">Mer information finns i [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d043-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d043-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6d043-132">INPUTS</span></span>

### <span data-ttu-id="6d043-133">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6d043-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6d043-134">System. String</span><span class="sxs-lookup"><span data-stu-id="6d043-134">System.String</span></span>

### <span data-ttu-id="6d043-135">System. byte []</span><span class="sxs-lookup"><span data-stu-id="6d043-135">System.Byte[]</span></span>

## <span data-ttu-id="6d043-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6d043-136">OUTPUTS</span></span>

### <span data-ttu-id="6d043-137">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="6d043-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="6d043-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6d043-138">NOTES</span></span>

## <span data-ttu-id="6d043-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6d043-139">RELATED LINKS</span></span>

[<span data-ttu-id="6d043-140">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="6d043-140">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="6d043-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="6d043-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="6d043-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="6d043-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


