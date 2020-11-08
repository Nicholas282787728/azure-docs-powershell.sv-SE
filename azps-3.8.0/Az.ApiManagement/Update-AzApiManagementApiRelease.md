---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: 99ec1234eea582fb91f2722032cb23c27e86b878
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94091888"
---
# <span data-ttu-id="07251-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="07251-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="07251-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="07251-102">SYNOPSIS</span></span>
<span data-ttu-id="07251-103">Uppdaterar en viss API-version.</span><span class="sxs-lookup"><span data-stu-id="07251-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="07251-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="07251-104">SYNTAX</span></span>

### <span data-ttu-id="07251-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="07251-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07251-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="07251-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07251-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="07251-107">DESCRIPTION</span></span>
<span data-ttu-id="07251-108">Cmdleten **Update-AzApiManagementApiRelease** ändrar en version av Azure API Management API.</span><span class="sxs-lookup"><span data-stu-id="07251-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="07251-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="07251-109">EXAMPLES</span></span>

### <span data-ttu-id="07251-110">Exempel 1: uppdaterar en API-version för en API-revision</span><span class="sxs-lookup"><span data-stu-id="07251-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="07251-111">Det här kommandot uppdaterar `echo-api-release` API-versionen av API: et `echo-api` med ny anteckning.</span><span class="sxs-lookup"><span data-stu-id="07251-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="07251-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="07251-112">PARAMETERS</span></span>

### <span data-ttu-id="07251-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="07251-113">-ApiId</span></span>
<span data-ttu-id="07251-114">Identifierare för befintligt API.</span><span class="sxs-lookup"><span data-stu-id="07251-114">Identifier of existing API.</span></span>
<span data-ttu-id="07251-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="07251-115">This parameter is required.</span></span>

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

### <span data-ttu-id="07251-116">-Kontext</span><span class="sxs-lookup"><span data-stu-id="07251-116">-Context</span></span>
<span data-ttu-id="07251-117">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="07251-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="07251-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="07251-118">This parameter is required.</span></span>

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

### <span data-ttu-id="07251-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07251-119">-DefaultProfile</span></span>
<span data-ttu-id="07251-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="07251-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07251-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07251-121">-InputObject</span></span>
<span data-ttu-id="07251-122">Instans av Skriv Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="07251-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

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

### <span data-ttu-id="07251-123">-Obs!</span><span class="sxs-lookup"><span data-stu-id="07251-123">-Note</span></span>
<span data-ttu-id="07251-124">API-versions anteckningar.</span><span class="sxs-lookup"><span data-stu-id="07251-124">Api Release Notes.</span></span>
<span data-ttu-id="07251-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="07251-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="07251-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07251-126">-PassThru</span></span>
<span data-ttu-id="07251-127">Om det anges kommer instansen av Microsoft. Azure. kommandon. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease typ som representerar set API-versionen.</span><span class="sxs-lookup"><span data-stu-id="07251-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="07251-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="07251-128">-ReleaseId</span></span>
<span data-ttu-id="07251-129">ID för ReleaseId för API-revision.</span><span class="sxs-lookup"><span data-stu-id="07251-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="07251-130">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="07251-130">This parameter is required.</span></span>

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

### <span data-ttu-id="07251-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="07251-131">-Confirm</span></span>
<span data-ttu-id="07251-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="07251-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07251-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07251-133">-WhatIf</span></span>
<span data-ttu-id="07251-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="07251-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07251-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="07251-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07251-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07251-136">CommonParameters</span></span>
<span data-ttu-id="07251-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07251-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07251-138">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07251-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07251-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="07251-139">INPUTS</span></span>

### <span data-ttu-id="07251-140">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="07251-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="07251-141">System. String</span><span class="sxs-lookup"><span data-stu-id="07251-141">System.String</span></span>

### <span data-ttu-id="07251-142">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="07251-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="07251-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="07251-143">OUTPUTS</span></span>

### <span data-ttu-id="07251-144">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="07251-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="07251-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="07251-145">NOTES</span></span>

## <span data-ttu-id="07251-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="07251-146">RELATED LINKS</span></span>

[<span data-ttu-id="07251-147">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="07251-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="07251-148">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="07251-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)
