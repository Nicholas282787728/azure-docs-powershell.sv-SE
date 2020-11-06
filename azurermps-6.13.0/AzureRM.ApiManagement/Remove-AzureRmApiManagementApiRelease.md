---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 71256ab72d8c5c6042aa6c17b184066f96b3a813
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573075"
---
# <span data-ttu-id="2bc32-101">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="2bc32-101">Remove-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="2bc32-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2bc32-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc32-103">Tar bort en viss API-version</span><span class="sxs-lookup"><span data-stu-id="2bc32-103">Removes a particular API Release</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bc32-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2bc32-104">SYNTAX</span></span>

### <span data-ttu-id="2bc32-105">ByApiReleaseId (standard)</span><span class="sxs-lookup"><span data-stu-id="2bc32-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bc32-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2bc32-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bc32-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2bc32-107">DESCRIPTION</span></span>

<span data-ttu-id="2bc32-108">Cmdleten **Remove-AzureRmApiManagementApiRelease** tar bort en befintlig API-utgåva.</span><span class="sxs-lookup"><span data-stu-id="2bc32-108">The **Remove-AzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="2bc32-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2bc32-109">EXAMPLES</span></span>

### <span data-ttu-id="2bc32-110">Exempel 1: ta bort en API-utgåva</span><span class="sxs-lookup"><span data-stu-id="2bc32-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="2bc32-111">Det här kommandot tar bort API-versionen med angivet ApiId och ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="2bc32-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="2bc32-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2bc32-112">PARAMETERS</span></span>

### <span data-ttu-id="2bc32-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="2bc32-113">-ApiId</span></span>
<span data-ttu-id="2bc32-114">ID för API: t.</span><span class="sxs-lookup"><span data-stu-id="2bc32-114">Identifier of the API.</span></span>
<span data-ttu-id="2bc32-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="2bc32-115">This parameter is required.</span></span>

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

### <span data-ttu-id="2bc32-116">-Kontext</span><span class="sxs-lookup"><span data-stu-id="2bc32-116">-Context</span></span>
<span data-ttu-id="2bc32-117">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2bc32-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2bc32-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="2bc32-118">This parameter is required.</span></span>

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

### <span data-ttu-id="2bc32-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc32-119">-DefaultProfile</span></span>
<span data-ttu-id="2bc32-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2bc32-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bc32-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2bc32-121">-InputObject</span></span>
<span data-ttu-id="2bc32-122">Instans av PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="2bc32-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="2bc32-123">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="2bc32-123">This parameter is required.</span></span>

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

### <span data-ttu-id="2bc32-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2bc32-124">-PassThru</span></span>
<span data-ttu-id="2bc32-125">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="2bc32-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="2bc32-126">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="2bc32-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="2bc32-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="2bc32-127">-ReleaseId</span></span>
<span data-ttu-id="2bc32-128">Identifierare för API-versionen.</span><span class="sxs-lookup"><span data-stu-id="2bc32-128">Identifier of the API Release.</span></span>
<span data-ttu-id="2bc32-129">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="2bc32-129">This parameter is required.</span></span>

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

### <span data-ttu-id="2bc32-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2bc32-130">-Confirm</span></span>
<span data-ttu-id="2bc32-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2bc32-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bc32-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bc32-132">-WhatIf</span></span>
<span data-ttu-id="2bc32-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2bc32-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bc32-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2bc32-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bc32-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bc32-135">CommonParameters</span></span>
<span data-ttu-id="2bc32-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bc32-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bc32-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bc32-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bc32-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2bc32-138">INPUTS</span></span>

### <span data-ttu-id="2bc32-139">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2bc32-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2bc32-140">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="2bc32-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>
<span data-ttu-id="2bc32-141">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2bc32-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="2bc32-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2bc32-142">System.String</span></span>

## <span data-ttu-id="2bc32-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2bc32-143">OUTPUTS</span></span>

### <span data-ttu-id="2bc32-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2bc32-144">System.Boolean</span></span>

## <span data-ttu-id="2bc32-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2bc32-145">NOTES</span></span>

## <span data-ttu-id="2bc32-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2bc32-146">RELATED LINKS</span></span>

[<span data-ttu-id="2bc32-147">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="2bc32-147">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="2bc32-148">New-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="2bc32-148">New-AzureRmApiManagementApiRelease</span></span>](./New-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="2bc32-149">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="2bc32-149">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
