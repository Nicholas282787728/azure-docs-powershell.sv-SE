---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 9826de76a65fe097d2daba106bd74df5e94a730e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322548"
---
# <span data-ttu-id="dd66d-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="dd66d-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="dd66d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dd66d-102">SYNOPSIS</span></span>
<span data-ttu-id="dd66d-103">Får API-Management-certifikat konfigurerade för ömsesidig autentisering med Server delen i tjänsten.</span><span class="sxs-lookup"><span data-stu-id="dd66d-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="dd66d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dd66d-104">SYNTAX</span></span>

### <span data-ttu-id="dd66d-105">ContextParameterSet (standard)</span><span class="sxs-lookup"><span data-stu-id="dd66d-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd66d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd66d-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd66d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dd66d-107">DESCRIPTION</span></span>
<span data-ttu-id="dd66d-108">Cmdleten **Get-AzApiManagementCertificate** får alla Azure API Management-certifikat eller certifikat som du anger.</span><span class="sxs-lookup"><span data-stu-id="dd66d-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="dd66d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dd66d-109">EXAMPLES</span></span>

### <span data-ttu-id="dd66d-110">Exempel 1: Hämta alla certifikat</span><span class="sxs-lookup"><span data-stu-id="dd66d-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="dd66d-111">Det här kommandot får alla API-Management-certifikat.</span><span class="sxs-lookup"><span data-stu-id="dd66d-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="dd66d-112">Exempel 2: skaffa ett certifikat utifrån dess ID</span><span class="sxs-lookup"><span data-stu-id="dd66d-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="dd66d-113">Det här kommandot får API-hanteringskonsolen med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="dd66d-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="dd66d-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dd66d-114">PARAMETERS</span></span>

### <span data-ttu-id="dd66d-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="dd66d-115">-CertificateId</span></span>
<span data-ttu-id="dd66d-116">Anger ID för det certifikat som ska visas.</span><span class="sxs-lookup"><span data-stu-id="dd66d-116">Specifies the ID of the certificate to get.</span></span>

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

### <span data-ttu-id="dd66d-117">-Kontext</span><span class="sxs-lookup"><span data-stu-id="dd66d-117">-Context</span></span>
<span data-ttu-id="dd66d-118">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="dd66d-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd66d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd66d-119">-DefaultProfile</span></span>
<span data-ttu-id="dd66d-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="dd66d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd66d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd66d-121">-ResourceId</span></span>
<span data-ttu-id="dd66d-122">Resurs-ID för arm-certifikatet.</span><span class="sxs-lookup"><span data-stu-id="dd66d-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="dd66d-123">Om du anger ett certifikat för ID: till.</span><span class="sxs-lookup"><span data-stu-id="dd66d-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="dd66d-124">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="dd66d-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd66d-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dd66d-125">-Confirm</span></span>
<span data-ttu-id="dd66d-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dd66d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd66d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd66d-127">-WhatIf</span></span>
<span data-ttu-id="dd66d-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dd66d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd66d-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dd66d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd66d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd66d-130">CommonParameters</span></span>
<span data-ttu-id="dd66d-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd66d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd66d-132">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd66d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd66d-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dd66d-133">INPUTS</span></span>

### <span data-ttu-id="dd66d-134">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dd66d-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dd66d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="dd66d-135">System.String</span></span>

## <span data-ttu-id="dd66d-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dd66d-136">OUTPUTS</span></span>

### <span data-ttu-id="dd66d-137">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="dd66d-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="dd66d-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dd66d-138">NOTES</span></span>

## <span data-ttu-id="dd66d-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dd66d-139">RELATED LINKS</span></span>

[<span data-ttu-id="dd66d-140">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="dd66d-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="dd66d-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="dd66d-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="dd66d-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="dd66d-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)

