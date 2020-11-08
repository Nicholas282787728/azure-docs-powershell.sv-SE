---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: 13f5297efc19aa56cc5af55962c072f5ff2a32d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271099"
---
# <span data-ttu-id="c2963-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c2963-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="c2963-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c2963-102">SYNOPSIS</span></span>
<span data-ttu-id="c2963-103">Tar bort ett API.</span><span class="sxs-lookup"><span data-stu-id="c2963-103">Removes an API.</span></span>

## <span data-ttu-id="c2963-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c2963-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2963-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c2963-105">DESCRIPTION</span></span>
<span data-ttu-id="c2963-106">Cmdleten **Remove-AzApiManagementApi** tar bort ett befintligt API.</span><span class="sxs-lookup"><span data-stu-id="c2963-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="c2963-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c2963-107">EXAMPLES</span></span>

### <span data-ttu-id="c2963-108">Exempel 1: ta bort ett API</span><span class="sxs-lookup"><span data-stu-id="c2963-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="c2963-109">Det här kommandot tar bort API: t med angivet ID.</span><span class="sxs-lookup"><span data-stu-id="c2963-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="c2963-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c2963-110">PARAMETERS</span></span>

### <span data-ttu-id="c2963-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c2963-111">-ApiId</span></span>
<span data-ttu-id="c2963-112">Anger ID: t för API Remove.</span><span class="sxs-lookup"><span data-stu-id="c2963-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="c2963-113">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c2963-113">-Context</span></span>
<span data-ttu-id="c2963-114">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="c2963-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c2963-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2963-115">-DefaultProfile</span></span>
<span data-ttu-id="c2963-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c2963-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2963-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2963-117">-PassThru</span></span>
<span data-ttu-id="c2963-118">passthru</span><span class="sxs-lookup"><span data-stu-id="c2963-118">passthru</span></span>

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

### <span data-ttu-id="c2963-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c2963-119">-Confirm</span></span>
<span data-ttu-id="c2963-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c2963-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2963-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2963-121">-WhatIf</span></span>
<span data-ttu-id="c2963-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c2963-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2963-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c2963-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2963-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2963-124">CommonParameters</span></span>
<span data-ttu-id="c2963-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2963-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2963-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2963-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2963-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c2963-127">INPUTS</span></span>

### <span data-ttu-id="c2963-128">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c2963-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c2963-129">System. String</span><span class="sxs-lookup"><span data-stu-id="c2963-129">System.String</span></span>

### <span data-ttu-id="c2963-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c2963-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c2963-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c2963-131">OUTPUTS</span></span>

### <span data-ttu-id="c2963-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2963-132">System.Boolean</span></span>

## <span data-ttu-id="c2963-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c2963-133">NOTES</span></span>

## <span data-ttu-id="c2963-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c2963-134">RELATED LINKS</span></span>

[<span data-ttu-id="c2963-135">Exportera-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c2963-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="c2963-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c2963-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="c2963-137">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c2963-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="c2963-138">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c2963-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="c2963-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c2963-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


