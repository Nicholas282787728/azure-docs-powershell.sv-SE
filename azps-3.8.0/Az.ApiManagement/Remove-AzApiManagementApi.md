---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: 13f5297efc19aa56cc5af55962c072f5ff2a32d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089923"
---
# <span data-ttu-id="d1fe0-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d1fe0-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="d1fe0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d1fe0-102">SYNOPSIS</span></span>
<span data-ttu-id="d1fe0-103">Tar bort ett API.</span><span class="sxs-lookup"><span data-stu-id="d1fe0-103">Removes an API.</span></span>

## <span data-ttu-id="d1fe0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d1fe0-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1fe0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d1fe0-105">DESCRIPTION</span></span>
<span data-ttu-id="d1fe0-106">Cmdleten **Remove-AzApiManagementApi** tar bort ett befintligt API.</span><span class="sxs-lookup"><span data-stu-id="d1fe0-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="d1fe0-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d1fe0-107">EXAMPLES</span></span>

### <span data-ttu-id="d1fe0-108">Exempel 1: ta bort ett API</span><span class="sxs-lookup"><span data-stu-id="d1fe0-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="d1fe0-109">Det här kommandot tar bort API: t med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="d1fe0-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="d1fe0-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d1fe0-110">PARAMETERS</span></span>

### <span data-ttu-id="d1fe0-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d1fe0-111">-ApiId</span></span>
<span data-ttu-id="d1fe0-112">Anger ID: t för API Remove.</span><span class="sxs-lookup"><span data-stu-id="d1fe0-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="d1fe0-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="d1fe0-113">-Context</span></span>
<span data-ttu-id="d1fe0-114">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="d1fe0-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d1fe0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1fe0-115">-DefaultProfile</span></span>
<span data-ttu-id="d1fe0-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d1fe0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1fe0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1fe0-117">-PassThru</span></span>
<span data-ttu-id="d1fe0-118">passthru</span><span class="sxs-lookup"><span data-stu-id="d1fe0-118">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1fe0-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d1fe0-119">-Confirm</span></span>
<span data-ttu-id="d1fe0-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d1fe0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1fe0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1fe0-121">-WhatIf</span></span>
<span data-ttu-id="d1fe0-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d1fe0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1fe0-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d1fe0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1fe0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1fe0-124">CommonParameters</span></span>
<span data-ttu-id="d1fe0-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1fe0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1fe0-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1fe0-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1fe0-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d1fe0-127">INPUTS</span></span>

### <span data-ttu-id="d1fe0-128">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d1fe0-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d1fe0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d1fe0-129">System.String</span></span>

### <span data-ttu-id="d1fe0-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d1fe0-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d1fe0-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d1fe0-131">OUTPUTS</span></span>

### <span data-ttu-id="d1fe0-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d1fe0-132">System.Boolean</span></span>

## <span data-ttu-id="d1fe0-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d1fe0-133">NOTES</span></span>

## <span data-ttu-id="d1fe0-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d1fe0-134">RELATED LINKS</span></span>

[<span data-ttu-id="d1fe0-135">Exportera-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d1fe0-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="d1fe0-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d1fe0-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="d1fe0-137">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d1fe0-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="d1fe0-138">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d1fe0-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="d1fe0-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="d1fe0-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


