---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: cd32f29a0202fa8c38abed43075a8623efe068a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573071"
---
# <span data-ttu-id="c21c5-101">Remove-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="c21c5-101">Remove-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="c21c5-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c21c5-102">SYNOPSIS</span></span>
<span data-ttu-id="c21c5-103">Tog bort en särskild API-revision</span><span class="sxs-lookup"><span data-stu-id="c21c5-103">Removed a particular API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c21c5-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c21c5-104">SYNTAX</span></span>

### <span data-ttu-id="c21c5-105">ByApiId (standard)</span><span class="sxs-lookup"><span data-stu-id="c21c5-105">ByApiId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c21c5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c21c5-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c21c5-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c21c5-107">DESCRIPTION</span></span>
<span data-ttu-id="c21c5-108">Med cmdlet **Remove-AzureRmApiManagementApiRevision** tas en särskild API-revision bort.</span><span class="sxs-lookup"><span data-stu-id="c21c5-108">The cmdlet **Remove-AzureRmApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="c21c5-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c21c5-109">EXAMPLES</span></span>

### <span data-ttu-id="c21c5-110">Exempel 1: ta bort en API-revision</span><span class="sxs-lookup"><span data-stu-id="c21c5-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="c21c5-111">Det här kommandot tar bort `2` ändringen av API: t `echo-api` från API Management Service.</span><span class="sxs-lookup"><span data-stu-id="c21c5-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

## <span data-ttu-id="c21c5-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c21c5-112">PARAMETERS</span></span>

### <span data-ttu-id="c21c5-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c21c5-113">-ApiId</span></span>
<span data-ttu-id="c21c5-114">ID för API: t.</span><span class="sxs-lookup"><span data-stu-id="c21c5-114">Identifier of the API.</span></span>
<span data-ttu-id="c21c5-115">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c21c5-115">This parameter is required.</span></span>

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

### <span data-ttu-id="c21c5-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="c21c5-116">-ApiRevision</span></span>
<span data-ttu-id="c21c5-117">ID för API-revision.</span><span class="sxs-lookup"><span data-stu-id="c21c5-117">Identifier of the API Revision.</span></span> <span data-ttu-id="c21c5-118">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c21c5-118">This parameter is required.</span></span>

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

### <span data-ttu-id="c21c5-119">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c21c5-119">-Context</span></span>
<span data-ttu-id="c21c5-120">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c21c5-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c21c5-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c21c5-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c21c5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c21c5-122">-DefaultProfile</span></span>
<span data-ttu-id="c21c5-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c21c5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c21c5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c21c5-124">-InputObject</span></span>
<span data-ttu-id="c21c5-125">Instans av PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="c21c5-125">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="c21c5-126">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c21c5-126">This parameter is required.</span></span>

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

### <span data-ttu-id="c21c5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c21c5-127">-PassThru</span></span>
<span data-ttu-id="c21c5-128">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="c21c5-128">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="c21c5-129">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c21c5-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="c21c5-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c21c5-130">-Confirm</span></span>
<span data-ttu-id="c21c5-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c21c5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c21c5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c21c5-132">-WhatIf</span></span>
<span data-ttu-id="c21c5-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c21c5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c21c5-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c21c5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c21c5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c21c5-135">CommonParameters</span></span>
<span data-ttu-id="c21c5-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c21c5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c21c5-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c21c5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c21c5-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c21c5-138">INPUTS</span></span>

### <span data-ttu-id="c21c5-139">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c21c5-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c21c5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c21c5-140">System.String</span></span>

### <span data-ttu-id="c21c5-141">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c21c5-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="c21c5-142">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c21c5-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c21c5-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c21c5-143">OUTPUTS</span></span>

### <span data-ttu-id="c21c5-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c21c5-144">System.Boolean</span></span>

## <span data-ttu-id="c21c5-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c21c5-145">NOTES</span></span>

## <span data-ttu-id="c21c5-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c21c5-146">RELATED LINKS</span></span>

[<span data-ttu-id="c21c5-147">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="c21c5-147">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="c21c5-148">New-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="c21c5-148">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="c21c5-149">Set-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="c21c5-149">Set-AzureRmApiManagementApiRevision</span></span>](./Set-AzureRmApiManagementApiRevision.md)
