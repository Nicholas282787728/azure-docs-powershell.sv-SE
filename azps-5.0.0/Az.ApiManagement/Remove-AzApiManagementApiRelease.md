---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 9673df14bdd0f5b7d0e946170a155231e8c4e751
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323453"
---
# <span data-ttu-id="5266d-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="5266d-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="5266d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5266d-102">SYNOPSIS</span></span>
<span data-ttu-id="5266d-103">Tar bort en viss API-version</span><span class="sxs-lookup"><span data-stu-id="5266d-103">Removes a particular API Release</span></span>

## <span data-ttu-id="5266d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5266d-104">SYNTAX</span></span>

### <span data-ttu-id="5266d-105">ByApiReleaseId (standard)</span><span class="sxs-lookup"><span data-stu-id="5266d-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5266d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5266d-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5266d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5266d-107">DESCRIPTION</span></span>

<span data-ttu-id="5266d-108">Cmdleten **Remove-AzAzureRmApiManagementApiRelease** tar bort en befintlig API-utgåva.</span><span class="sxs-lookup"><span data-stu-id="5266d-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="5266d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5266d-109">EXAMPLES</span></span>

### <span data-ttu-id="5266d-110">Exempel 1: ta bort en API-utgåva</span><span class="sxs-lookup"><span data-stu-id="5266d-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="5266d-111">Det här kommandot tar bort API-versionen med angivet ApiId och ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="5266d-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="5266d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5266d-112">PARAMETERS</span></span>

### <span data-ttu-id="5266d-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5266d-113">-ApiId</span></span>
<span data-ttu-id="5266d-114">ID för API: t.</span><span class="sxs-lookup"><span data-stu-id="5266d-114">Identifier of the API.</span></span>
<span data-ttu-id="5266d-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="5266d-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5266d-116">-Kontext</span><span class="sxs-lookup"><span data-stu-id="5266d-116">-Context</span></span>
<span data-ttu-id="5266d-117">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="5266d-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5266d-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="5266d-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5266d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5266d-119">-DefaultProfile</span></span>
<span data-ttu-id="5266d-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="5266d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5266d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5266d-121">-InputObject</span></span>
<span data-ttu-id="5266d-122">Instans av PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="5266d-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="5266d-123">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="5266d-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5266d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5266d-124">-PassThru</span></span>
<span data-ttu-id="5266d-125">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="5266d-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="5266d-126">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="5266d-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="5266d-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="5266d-127">-ReleaseId</span></span>
<span data-ttu-id="5266d-128">Identifierare för API-versionen.</span><span class="sxs-lookup"><span data-stu-id="5266d-128">Identifier of the API Release.</span></span>
<span data-ttu-id="5266d-129">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="5266d-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5266d-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5266d-130">-Confirm</span></span>
<span data-ttu-id="5266d-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5266d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5266d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5266d-132">-WhatIf</span></span>
<span data-ttu-id="5266d-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5266d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5266d-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5266d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5266d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5266d-135">CommonParameters</span></span>
<span data-ttu-id="5266d-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5266d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5266d-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5266d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5266d-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5266d-138">INPUTS</span></span>

### <span data-ttu-id="5266d-139">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5266d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5266d-140">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="5266d-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="5266d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="5266d-141">System.String</span></span>

## <span data-ttu-id="5266d-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5266d-142">OUTPUTS</span></span>

### <span data-ttu-id="5266d-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5266d-143">System.Boolean</span></span>

## <span data-ttu-id="5266d-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5266d-144">NOTES</span></span>

## <span data-ttu-id="5266d-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5266d-145">RELATED LINKS</span></span>

[<span data-ttu-id="5266d-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="5266d-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="5266d-147">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="5266d-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="5266d-148">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="5266d-148">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)