---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 5b863c0d0c808c8cb993e4f78f9767d13fb634d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574059"
---
# <span data-ttu-id="cd091-101">Update-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cd091-101">Update-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="cd091-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cd091-102">SYNOPSIS</span></span>
<span data-ttu-id="cd091-103">Uppdaterar en viss API-version.</span><span class="sxs-lookup"><span data-stu-id="cd091-103">Updates a particular Api Release.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd091-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cd091-104">SYNTAX</span></span>

### <span data-ttu-id="cd091-105">ExpandedParameter (standard)</span><span class="sxs-lookup"><span data-stu-id="cd091-105">ExpandedParameter (Default)</span></span>
```
Update-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd091-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cd091-106">ByInputObject</span></span>
```
Update-AzureRmApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd091-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cd091-107">DESCRIPTION</span></span>
<span data-ttu-id="cd091-108">Cmdleten **Update-AzureRmApiManagementApiRelease** ändrar en version av Azure API Management API.</span><span class="sxs-lookup"><span data-stu-id="cd091-108">The **Update-AzureRmApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="cd091-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cd091-109">EXAMPLES</span></span>

### <span data-ttu-id="cd091-110">Exempel 1: uppdaterar en API-version för en API-revision</span><span class="sxs-lookup"><span data-stu-id="cd091-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="cd091-111">Det här kommandot uppdaterar `echo-api-release` API-versionen av API: et `echo-api` med ny anteckning.</span><span class="sxs-lookup"><span data-stu-id="cd091-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="cd091-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cd091-112">PARAMETERS</span></span>

### <span data-ttu-id="cd091-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="cd091-113">-ApiId</span></span>
<span data-ttu-id="cd091-114">Identifierare för befintligt API.</span><span class="sxs-lookup"><span data-stu-id="cd091-114">Identifier of existing API.</span></span>
<span data-ttu-id="cd091-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="cd091-115">This parameter is required.</span></span>

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

### <span data-ttu-id="cd091-116">-Kontext</span><span class="sxs-lookup"><span data-stu-id="cd091-116">-Context</span></span>
<span data-ttu-id="cd091-117">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="cd091-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="cd091-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="cd091-118">This parameter is required.</span></span>

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

### <span data-ttu-id="cd091-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd091-119">-DefaultProfile</span></span>
<span data-ttu-id="cd091-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cd091-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd091-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd091-121">-InputObject</span></span>
<span data-ttu-id="cd091-122">Instans av Skriv Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="cd091-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

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

### <span data-ttu-id="cd091-123">-Obs!</span><span class="sxs-lookup"><span data-stu-id="cd091-123">-Note</span></span>
<span data-ttu-id="cd091-124">API-versions anteckningar.</span><span class="sxs-lookup"><span data-stu-id="cd091-124">Api Release Notes.</span></span>
<span data-ttu-id="cd091-125">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="cd091-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="cd091-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd091-126">-PassThru</span></span>
<span data-ttu-id="cd091-127">Om det anges kommer instansen av Microsoft. Azure. kommandon. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease typ som representerar set API-versionen.</span><span class="sxs-lookup"><span data-stu-id="cd091-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="cd091-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="cd091-128">-ReleaseId</span></span>
<span data-ttu-id="cd091-129">ID för ReleaseId för API-revision.</span><span class="sxs-lookup"><span data-stu-id="cd091-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="cd091-130">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="cd091-130">This parameter is required.</span></span>

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

### <span data-ttu-id="cd091-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cd091-131">-Confirm</span></span>
<span data-ttu-id="cd091-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cd091-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd091-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd091-133">-WhatIf</span></span>
<span data-ttu-id="cd091-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cd091-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd091-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cd091-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd091-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd091-136">CommonParameters</span></span>
<span data-ttu-id="cd091-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd091-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd091-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd091-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd091-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cd091-139">INPUTS</span></span>

### <span data-ttu-id="cd091-140">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cd091-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="cd091-141">Parametrar: kontext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cd091-141">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="cd091-142">System. String</span><span class="sxs-lookup"><span data-stu-id="cd091-142">System.String</span></span>

### <span data-ttu-id="cd091-143">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cd091-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="cd091-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cd091-144">OUTPUTS</span></span>

### <span data-ttu-id="cd091-145">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cd091-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="cd091-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cd091-146">NOTES</span></span>

## <span data-ttu-id="cd091-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cd091-147">RELATED LINKS</span></span>

[<span data-ttu-id="cd091-148">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cd091-148">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="cd091-149">New-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="cd091-149">New-AzureRmApiManagementApiRelease</span></span>](./New-AzureRmApiManagementApiRelease.md)
