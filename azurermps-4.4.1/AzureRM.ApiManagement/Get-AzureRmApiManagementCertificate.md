---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 167137cbb231bbd5093b118a22d33e2102159c67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578696"
---
# <span data-ttu-id="9367d-101">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="9367d-101">Get-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="9367d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9367d-102">SYNOPSIS</span></span>
<span data-ttu-id="9367d-103">Hämtar API-Management-certifikat.</span><span class="sxs-lookup"><span data-stu-id="9367d-103">Gets API Management certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9367d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9367d-104">SYNTAX</span></span>

### <span data-ttu-id="9367d-105">Hämta alla certifikat (standard)</span><span class="sxs-lookup"><span data-stu-id="9367d-105">Get all certificates (Default)</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9367d-106">Skaffa certifikat utifrån ID</span><span class="sxs-lookup"><span data-stu-id="9367d-106">Get certificate by ID</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9367d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9367d-107">DESCRIPTION</span></span>
<span data-ttu-id="9367d-108">Cmdleten **Get-AzureRmApiManagementCertificate** får alla Azure API Management-certifikat eller certifikat som du anger.</span><span class="sxs-lookup"><span data-stu-id="9367d-108">The **Get-AzureRmApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="9367d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9367d-109">EXAMPLES</span></span>

### <span data-ttu-id="9367d-110">Exempel 1: Hämta alla certifikat</span><span class="sxs-lookup"><span data-stu-id="9367d-110">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="9367d-111">Det här kommandot får alla API-Management-certifikat.</span><span class="sxs-lookup"><span data-stu-id="9367d-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="9367d-112">Exempel 2: skaffa ett certifikat utifrån dess ID</span><span class="sxs-lookup"><span data-stu-id="9367d-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="9367d-113">Det här kommandot får API-hanteringskonsolen med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="9367d-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="9367d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9367d-114">PARAMETERS</span></span>

### <span data-ttu-id="9367d-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="9367d-115">-CertificateId</span></span>
<span data-ttu-id="9367d-116">Anger ID för det certifikat som ska visas.</span><span class="sxs-lookup"><span data-stu-id="9367d-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Get certificate by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9367d-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="9367d-117">-Context</span></span>
<span data-ttu-id="9367d-118">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="9367d-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9367d-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9367d-119">-Confirm</span></span>
<span data-ttu-id="9367d-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9367d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9367d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9367d-121">-WhatIf</span></span>
<span data-ttu-id="9367d-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9367d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9367d-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9367d-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9367d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9367d-124">-DefaultProfile</span></span>
<span data-ttu-id="9367d-125">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="9367d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9367d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9367d-126">CommonParameters</span></span>
<span data-ttu-id="9367d-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9367d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9367d-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9367d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9367d-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9367d-129">INPUTS</span></span>

## <span data-ttu-id="9367d-130">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9367d-130">OUTPUTS</span></span>

### <span data-ttu-id="9367d-131">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="9367d-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="9367d-132">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9367d-132">NOTES</span></span>

## <span data-ttu-id="9367d-133">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9367d-133">RELATED LINKS</span></span>

[<span data-ttu-id="9367d-134">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="9367d-134">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="9367d-135">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="9367d-135">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="9367d-136">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="9367d-136">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


