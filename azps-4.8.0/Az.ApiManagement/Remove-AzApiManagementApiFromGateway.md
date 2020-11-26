---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
ms.openlocfilehash: 506287812f684a778fdb96e750aac34049912b58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94261484"
---
# <span data-ttu-id="c9f7f-101">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="c9f7f-101">Remove-AzApiManagementApiFromGateway</span></span>

## <span data-ttu-id="c9f7f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c9f7f-102">SYNOPSIS</span></span>
<span data-ttu-id="c9f7f-103">Bifogar ett API till en gateway.</span><span class="sxs-lookup"><span data-stu-id="c9f7f-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="c9f7f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c9f7f-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9f7f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c9f7f-105">DESCRIPTION</span></span>
<span data-ttu-id="c9f7f-106">Cmdleten **Remove-AzApiManagementApiFromGateway** bifogar ett API till en gateway.</span><span class="sxs-lookup"><span data-stu-id="c9f7f-106">The **Remove-AzApiManagementApiFromGateway** cmdlet attaches an API to a gateway.</span></span>

## <span data-ttu-id="c9f7f-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c9f7f-107">EXAMPLES</span></span>

### <span data-ttu-id="c9f7f-108">Exempel 1: ta bort ett API från en gateway</span><span class="sxs-lookup"><span data-stu-id="c9f7f-108">Example 1: Remove an API from a gateway</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="c9f7f-109">Det här kommandot tar bort angivet API från en gateway.</span><span class="sxs-lookup"><span data-stu-id="c9f7f-109">This command removes the specified API from a gateway.</span></span>

## <span data-ttu-id="c9f7f-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c9f7f-110">PARAMETERS</span></span>

### <span data-ttu-id="c9f7f-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c9f7f-111">-ApiId</span></span>
<span data-ttu-id="c9f7f-112">Identifierare för befintliga API: er som ska tas bort från gatewayen.</span><span class="sxs-lookup"><span data-stu-id="c9f7f-112">Identifier of existing APIs to remove from the Gateway.</span></span>
<span data-ttu-id="c9f7f-113">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c9f7f-113">This parameter is required.</span></span>

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

### <span data-ttu-id="c9f7f-114">-Kontext</span><span class="sxs-lookup"><span data-stu-id="c9f7f-114">-Context</span></span>
<span data-ttu-id="c9f7f-115">Instans av PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c9f7f-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c9f7f-116">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c9f7f-116">This parameter is required.</span></span>

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

### <span data-ttu-id="c9f7f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9f7f-117">-DefaultProfile</span></span>
<span data-ttu-id="c9f7f-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c9f7f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9f7f-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="c9f7f-119">-GatewayId</span></span>
<span data-ttu-id="c9f7f-120">Identifierare för befintlig gateway att ta bort API från.</span><span class="sxs-lookup"><span data-stu-id="c9f7f-120">Identifier of existing Gateway to remove API from.</span></span>
<span data-ttu-id="c9f7f-121">Denna parameter är obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="c9f7f-121">This parameter is required.</span></span>

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

### <span data-ttu-id="c9f7f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9f7f-122">-PassThru</span></span>
<span data-ttu-id="c9f7f-123">Om det här värdet anges skrivs sant om-operationen lyckas.</span><span class="sxs-lookup"><span data-stu-id="c9f7f-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="c9f7f-124">Denna parameter är valfri.</span><span class="sxs-lookup"><span data-stu-id="c9f7f-124">This parameter is optional.</span></span>
<span data-ttu-id="c9f7f-125">Standardvärdet är falskt.</span><span class="sxs-lookup"><span data-stu-id="c9f7f-125">Default value is false.</span></span>

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

### <span data-ttu-id="c9f7f-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c9f7f-126">-Confirm</span></span>
<span data-ttu-id="c9f7f-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c9f7f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9f7f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9f7f-128">-WhatIf</span></span>
<span data-ttu-id="c9f7f-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c9f7f-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9f7f-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c9f7f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9f7f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9f7f-131">CommonParameters</span></span>
<span data-ttu-id="c9f7f-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9f7f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9f7f-133">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c9f7f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9f7f-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c9f7f-134">INPUTS</span></span>

### <span data-ttu-id="c9f7f-135">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c9f7f-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c9f7f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c9f7f-136">System.String</span></span>

### <span data-ttu-id="c9f7f-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c9f7f-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c9f7f-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c9f7f-138">OUTPUTS</span></span>

### <span data-ttu-id="c9f7f-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c9f7f-139">System.Boolean</span></span>

## <span data-ttu-id="c9f7f-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c9f7f-140">NOTES</span></span>

## <span data-ttu-id="c9f7f-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c9f7f-141">RELATED LINKS</span></span>