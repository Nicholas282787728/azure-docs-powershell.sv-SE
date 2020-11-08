---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 80B61E7D-14DC-422A-8EE3-CAC49EF1BE8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: ab278dcf56646463e1ccbc8ada9baa896b1759bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271091"
---
# <span data-ttu-id="f4eaa-101">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f4eaa-101">Remove-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="f4eaa-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="f4eaa-103">Tar bort en OpenID Connect-leverantör.</span><span class="sxs-lookup"><span data-stu-id="f4eaa-103">Removes an OpenID Connect provider.</span></span>

## <span data-ttu-id="f4eaa-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4eaa-104">SYNTAX</span></span>

```
Remove-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4eaa-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4eaa-105">DESCRIPTION</span></span>
<span data-ttu-id="f4eaa-106">Cmdleten **Remove-AzApiManagementOpenIdConnectProvider** tar bort en OpenID Connect-leverantör för Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="f4eaa-106">The **Remove-AzApiManagementOpenIdConnectProvider** cmdlet removes an OpenID Connect provider for Azure API Management.</span></span>

## <span data-ttu-id="f4eaa-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4eaa-107">EXAMPLES</span></span>

### <span data-ttu-id="f4eaa-108">Exempel 1: ta bort en leverantör</span><span class="sxs-lookup"><span data-stu-id="f4eaa-108">Example 1: Remove a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -PassThru
```

<span data-ttu-id="f4eaa-109">Det här kommandot tar bort en Provider med ID-OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="f4eaa-109">This command removes a provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="f4eaa-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4eaa-110">PARAMETERS</span></span>

### <span data-ttu-id="f4eaa-111">-Kontext</span><span class="sxs-lookup"><span data-stu-id="f4eaa-111">-Context</span></span>
<span data-ttu-id="f4eaa-112">Anger ett **PsApiManagementContext** -objekt.</span><span class="sxs-lookup"><span data-stu-id="f4eaa-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f4eaa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4eaa-113">-DefaultProfile</span></span>
<span data-ttu-id="f4eaa-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="f4eaa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4eaa-115">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="f4eaa-115">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="f4eaa-116">Anger ett ID för den provider som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="f4eaa-116">Specifies an ID of the provider that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f4eaa-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4eaa-117">-PassThru</span></span>
<span data-ttu-id="f4eaa-118">Anger att denna cmdlet returnerar ett värde för $True om åtgärden lyckas eller $False på annat sätt.</span><span class="sxs-lookup"><span data-stu-id="f4eaa-118">Indicates that this cmdlet returns a value of $True if the operation succeeds or $False otherwise.</span></span>

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

### <span data-ttu-id="f4eaa-119">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f4eaa-119">-Confirm</span></span>
<span data-ttu-id="f4eaa-120">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f4eaa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4eaa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4eaa-121">-WhatIf</span></span>
<span data-ttu-id="f4eaa-122">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f4eaa-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4eaa-123">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f4eaa-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4eaa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4eaa-124">CommonParameters</span></span>
<span data-ttu-id="f4eaa-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4eaa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4eaa-126">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4eaa-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4eaa-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4eaa-127">INPUTS</span></span>

### <span data-ttu-id="f4eaa-128">Microsoft. Azure. commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f4eaa-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f4eaa-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f4eaa-129">System.String</span></span>

### <span data-ttu-id="f4eaa-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f4eaa-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f4eaa-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4eaa-131">OUTPUTS</span></span>

### <span data-ttu-id="f4eaa-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f4eaa-132">System.Boolean</span></span>

## <span data-ttu-id="f4eaa-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4eaa-133">NOTES</span></span>

## <span data-ttu-id="f4eaa-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4eaa-134">RELATED LINKS</span></span>

[<span data-ttu-id="f4eaa-135">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f4eaa-135">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="f4eaa-136">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f4eaa-136">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="f4eaa-137">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f4eaa-137">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


