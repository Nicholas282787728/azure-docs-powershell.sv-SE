---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: aa8c40d7fb9f5ccb99ccdd88d6c04ceb4a888bf2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401216"
---
# <span data-ttu-id="d3368-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3368-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="d3368-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d3368-102">SYNOPSIS</span></span>
<span data-ttu-id="d3368-103">Tar bort en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d3368-103">Removes an application gateway.</span></span>

## <span data-ttu-id="d3368-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d3368-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3368-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d3368-105">DESCRIPTION</span></span>
<span data-ttu-id="d3368-106">Cmdleten **Remove-AzApplicationGateway** tar bort en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="d3368-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="d3368-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d3368-107">EXAMPLES</span></span>

### <span data-ttu-id="d3368-108">Exempel 1: ta bort en angiven Programgateway</span><span class="sxs-lookup"><span data-stu-id="d3368-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d3368-109">Det här kommandot tar bort den Programgateway som heter ApplicationGateway01 i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="d3368-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="d3368-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d3368-110">PARAMETERS</span></span>

### <span data-ttu-id="d3368-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3368-111">-DefaultProfile</span></span>
<span data-ttu-id="d3368-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="d3368-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3368-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d3368-113">-Force</span></span>
<span data-ttu-id="d3368-114">Anger att cmdleten tvingar bort Application Gateway, oavsett om det är tilldelat resurser eller inte.</span><span class="sxs-lookup"><span data-stu-id="d3368-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="d3368-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="d3368-115">-Name</span></span>
<span data-ttu-id="d3368-116">Anger namnet på den Programgateway som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="d3368-116">Specifies the name of the application gateway to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3368-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3368-117">-PassThru</span></span>
<span data-ttu-id="d3368-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="d3368-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d3368-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="d3368-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d3368-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3368-120">-ResourceGroupName</span></span>
<span data-ttu-id="d3368-121">Anger namnet på resurs grupps namnet som applikations-gatewayen tillhör.</span><span class="sxs-lookup"><span data-stu-id="d3368-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="d3368-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d3368-122">-Confirm</span></span>
<span data-ttu-id="d3368-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d3368-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3368-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3368-124">-WhatIf</span></span>
<span data-ttu-id="d3368-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d3368-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3368-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d3368-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3368-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3368-127">CommonParameters</span></span>
<span data-ttu-id="d3368-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3368-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3368-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3368-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3368-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d3368-130">INPUTS</span></span>

### <span data-ttu-id="d3368-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d3368-131">System.String</span></span>

### <span data-ttu-id="d3368-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d3368-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d3368-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d3368-133">OUTPUTS</span></span>

### <span data-ttu-id="d3368-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d3368-134">System.Boolean</span></span>

## <span data-ttu-id="d3368-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d3368-135">NOTES</span></span>

## <span data-ttu-id="d3368-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d3368-136">RELATED LINKS</span></span>

[<span data-ttu-id="d3368-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3368-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


