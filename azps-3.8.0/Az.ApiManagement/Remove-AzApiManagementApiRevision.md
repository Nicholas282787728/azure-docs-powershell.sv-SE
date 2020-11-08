---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRevision.md
ms.openlocfilehash: 32677a5b8c3383b23b6ebb9832842f410a74532f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090627"
---
# <span data-ttu-id="d94f0-101">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="d94f0-101">Remove-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="d94f0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d94f0-102">SYNOPSIS</span></span>
<span data-ttu-id="d94f0-103">Tog bort en särskild API-revision</span><span class="sxs-lookup"><span data-stu-id="d94f0-103">Removed a particular API Revision</span></span>

## <span data-ttu-id="d94f0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d94f0-104">SYNTAX</span></span>

### <span data-ttu-id="d94f0-105">ByApiId (standard)</span><span class="sxs-lookup"><span data-stu-id="d94f0-105">ByApiId (Default)</span></span>
```
Remove-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d94f0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d94f0-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d94f0-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d94f0-107">DESCRIPTION</span></span>
<span data-ttu-id="d94f0-108">Med cmdlet **Remove-AzApiManagementApiRevision** tas en särskild API-revision bort.</span><span class="sxs-lookup"><span data-stu-id="d94f0-108">The cmdlet **Remove-AzApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="d94f0-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d94f0-109">EXAMPLES</span></span>

### <span data-ttu-id="d94f0-110">Exempel 1: ta bort en API-revision</span><span class="sxs-lookup"><span data-stu-id="d94f0-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="d94f0-111">Det här kommandot tar bort `2` ändringen av API: t `echo-api` från API Management Service.</span><span class="sxs-lookup"><span data-stu-id="d94f0-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

## <span data-ttu-id="d94f0-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d94f0-112">PARAMETERS</span></span>

### <span data-ttu-id="d94f0-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d94f0-113">-ApiId</span></span>
<span data-ttu-id="d94f0-114">ID för API: t.</span><span class="sxs-lookup"><span data-stu-id="d94f0-114">Identifier of the API.</span></span>
<span data-ttu-id="d94f0-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d94f0-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d94f0-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d94f0-116">-ApiRevision</span></span>
<span data-ttu-id="d94f0-117">ID för API-revision.</span><span class="sxs-lookup"><span data-stu-id="d94f0-117">Identifier of the API Revision.</span></span> <span data-ttu-id="d94f0-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d94f0-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d94f0-119">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d94f0-119">-Context</span></span>
<span data-ttu-id="d94f0-120">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d94f0-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d94f0-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d94f0-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d94f0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d94f0-122">-DefaultProfile</span></span>
<span data-ttu-id="d94f0-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d94f0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d94f0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d94f0-124">-InputObject</span></span>
<span data-ttu-id="d94f0-125">Instans av PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="d94f0-125">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="d94f0-126">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="d94f0-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d94f0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d94f0-127">-PassThru</span></span>
<span data-ttu-id="d94f0-128">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="d94f0-128">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="d94f0-129">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="d94f0-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="d94f0-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d94f0-130">-Confirm</span></span>
<span data-ttu-id="d94f0-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d94f0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d94f0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d94f0-132">-WhatIf</span></span>
<span data-ttu-id="d94f0-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d94f0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d94f0-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d94f0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d94f0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d94f0-135">CommonParameters</span></span>
<span data-ttu-id="d94f0-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d94f0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d94f0-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d94f0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d94f0-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d94f0-138">INPUTS</span></span>

### <span data-ttu-id="d94f0-139">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d94f0-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d94f0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d94f0-140">System.String</span></span>

### <span data-ttu-id="d94f0-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d94f0-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="d94f0-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d94f0-142">OUTPUTS</span></span>

### <span data-ttu-id="d94f0-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d94f0-143">System.Boolean</span></span>

## <span data-ttu-id="d94f0-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d94f0-144">NOTES</span></span>

## <span data-ttu-id="d94f0-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d94f0-145">RELATED LINKS</span></span>

[<span data-ttu-id="d94f0-146">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="d94f0-146">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="d94f0-147">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="d94f0-147">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="d94f0-148">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="d94f0-148">Set-AzApiManagementApiRevision</span></span>](./Set-AzApiManagementApiRevision.md)