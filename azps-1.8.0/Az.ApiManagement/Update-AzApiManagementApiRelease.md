---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: f6f042f26f5dede90db77e8c373e337f00755001
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917654"
---
# <span data-ttu-id="bd013-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bd013-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="bd013-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd013-102">SYNOPSIS</span></span>
<span data-ttu-id="bd013-103">Uppdaterar en viss API-version.</span><span class="sxs-lookup"><span data-stu-id="bd013-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="bd013-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd013-104">SYNTAX</span></span>

### <span data-ttu-id="bd013-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="bd013-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd013-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bd013-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd013-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd013-107">DESCRIPTION</span></span>
<span data-ttu-id="bd013-108">Cmdleten **Update-AzApiManagementApiRelease** ändrar en version av Azure API Management API.</span><span class="sxs-lookup"><span data-stu-id="bd013-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="bd013-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd013-109">EXAMPLES</span></span>

### <span data-ttu-id="bd013-110">Exempel 1: uppdaterar en API-version för en API-revision</span><span class="sxs-lookup"><span data-stu-id="bd013-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="bd013-111">Det här kommandot uppdaterar `echo-api-release` API-versionen av API: et `echo-api` med ny anteckning.</span><span class="sxs-lookup"><span data-stu-id="bd013-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="bd013-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd013-112">PARAMETERS</span></span>

### <span data-ttu-id="bd013-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bd013-113">-ApiId</span></span>
<span data-ttu-id="bd013-114">Identifierare för befintligt API.</span><span class="sxs-lookup"><span data-stu-id="bd013-114">Identifier of existing API.</span></span>
<span data-ttu-id="bd013-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="bd013-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd013-116">-Kontext</span><span class="sxs-lookup"><span data-stu-id="bd013-116">-Context</span></span>
<span data-ttu-id="bd013-117">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="bd013-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bd013-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="bd013-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd013-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd013-119">-DefaultProfile</span></span>
<span data-ttu-id="bd013-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd013-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd013-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd013-121">-InputObject</span></span>
<span data-ttu-id="bd013-122">Instans av Skriv Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="bd013-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd013-123">-Obs!</span><span class="sxs-lookup"><span data-stu-id="bd013-123">-Note</span></span>
<span data-ttu-id="bd013-124">API-versions anteckningar.</span><span class="sxs-lookup"><span data-stu-id="bd013-124">Api Release Notes.</span></span>
<span data-ttu-id="bd013-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="bd013-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="bd013-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd013-126">-PassThru</span></span>
<span data-ttu-id="bd013-127">Om det anges kommer instansen av Microsoft. Azure. kommandon. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease typ som representerar set API-versionen.</span><span class="sxs-lookup"><span data-stu-id="bd013-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd013-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="bd013-128">-ReleaseId</span></span>
<span data-ttu-id="bd013-129">ID för ReleaseId för API-revision.</span><span class="sxs-lookup"><span data-stu-id="bd013-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="bd013-130">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="bd013-130">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd013-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bd013-131">-Confirm</span></span>
<span data-ttu-id="bd013-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bd013-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd013-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd013-133">-WhatIf</span></span>
<span data-ttu-id="bd013-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bd013-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd013-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bd013-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd013-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd013-136">CommonParameters</span></span>
<span data-ttu-id="bd013-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd013-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd013-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd013-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd013-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd013-139">INPUTS</span></span>

### <span data-ttu-id="bd013-140">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bd013-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bd013-141">System. String</span><span class="sxs-lookup"><span data-stu-id="bd013-141">System.String</span></span>

### <span data-ttu-id="bd013-142">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bd013-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="bd013-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd013-143">OUTPUTS</span></span>

### <span data-ttu-id="bd013-144">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bd013-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="bd013-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd013-145">NOTES</span></span>

## <span data-ttu-id="bd013-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd013-146">RELATED LINKS</span></span>

[<span data-ttu-id="bd013-147">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bd013-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="bd013-148">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="bd013-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)
