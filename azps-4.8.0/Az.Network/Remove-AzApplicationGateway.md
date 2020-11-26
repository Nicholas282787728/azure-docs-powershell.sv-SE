---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: aa8c40d7fb9f5ccb99ccdd88d6c04ceb4a888bf2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94262076"
---
# <span data-ttu-id="fb51a-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb51a-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="fb51a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="fb51a-102">SYNOPSIS</span></span>
<span data-ttu-id="fb51a-103">Tar bort en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="fb51a-103">Removes an application gateway.</span></span>

## <span data-ttu-id="fb51a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="fb51a-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb51a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="fb51a-105">DESCRIPTION</span></span>
<span data-ttu-id="fb51a-106">Cmdleten **Remove-AzApplicationGateway** tar bort en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="fb51a-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="fb51a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="fb51a-107">EXAMPLES</span></span>

### <span data-ttu-id="fb51a-108">Exempel 1: ta bort en angiven Programgateway</span><span class="sxs-lookup"><span data-stu-id="fb51a-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fb51a-109">Det här kommandot tar bort den Programgateway som heter ApplicationGateway01 i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="fb51a-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="fb51a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="fb51a-110">PARAMETERS</span></span>

### <span data-ttu-id="fb51a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb51a-111">-DefaultProfile</span></span>
<span data-ttu-id="fb51a-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="fb51a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb51a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fb51a-113">-Force</span></span>
<span data-ttu-id="fb51a-114">Anger att cmdleten tvingar bort Application Gateway, oavsett om det är tilldelat resurser eller inte.</span><span class="sxs-lookup"><span data-stu-id="fb51a-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="fb51a-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="fb51a-115">-Name</span></span>
<span data-ttu-id="fb51a-116">Anger namnet på den Programgateway som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="fb51a-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="fb51a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb51a-117">-PassThru</span></span>
<span data-ttu-id="fb51a-118">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="fb51a-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fb51a-119">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="fb51a-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fb51a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb51a-120">-ResourceGroupName</span></span>
<span data-ttu-id="fb51a-121">Anger namnet på resurs grupps namnet som applikations-gatewayen tillhör.</span><span class="sxs-lookup"><span data-stu-id="fb51a-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="fb51a-122">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="fb51a-122">-Confirm</span></span>
<span data-ttu-id="fb51a-123">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="fb51a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb51a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb51a-124">-WhatIf</span></span>
<span data-ttu-id="fb51a-125">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="fb51a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb51a-126">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="fb51a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb51a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb51a-127">CommonParameters</span></span>
<span data-ttu-id="fb51a-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb51a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb51a-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb51a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb51a-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="fb51a-130">INPUTS</span></span>

### <span data-ttu-id="fb51a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="fb51a-131">System.String</span></span>

### <span data-ttu-id="fb51a-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fb51a-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fb51a-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="fb51a-133">OUTPUTS</span></span>

### <span data-ttu-id="fb51a-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fb51a-134">System.Boolean</span></span>

## <span data-ttu-id="fb51a-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="fb51a-135">NOTES</span></span>

## <span data-ttu-id="fb51a-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="fb51a-136">RELATED LINKS</span></span>

[<span data-ttu-id="fb51a-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fb51a-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

