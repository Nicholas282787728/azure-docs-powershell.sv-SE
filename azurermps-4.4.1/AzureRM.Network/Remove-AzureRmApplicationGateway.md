---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
ms.openlocfilehash: cd4824b73aa7fe7a80a3c4bccba37445a85c2c22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574581"
---
# <span data-ttu-id="8c21a-101">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8c21a-101">Remove-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="8c21a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="8c21a-102">SYNOPSIS</span></span>
<span data-ttu-id="8c21a-103">Tar bort en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="8c21a-103">Removes an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c21a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="8c21a-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c21a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="8c21a-105">DESCRIPTION</span></span>
<span data-ttu-id="8c21a-106">Cmdleten **Remove-AzureRmApplicationGateway** tar bort en Programgateway.</span><span class="sxs-lookup"><span data-stu-id="8c21a-106">The **Remove-AzureRmApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="8c21a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="8c21a-107">EXAMPLES</span></span>

### <span data-ttu-id="8c21a-108">Exempel 1: ta bort en angiven Programgateway</span><span class="sxs-lookup"><span data-stu-id="8c21a-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8c21a-109">Det här kommandot tar bort den Programgateway som heter ApplicationGateway01 i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="8c21a-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="8c21a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="8c21a-110">PARAMETERS</span></span>

### <span data-ttu-id="8c21a-111">-Force</span><span class="sxs-lookup"><span data-stu-id="8c21a-111">-Force</span></span>
<span data-ttu-id="8c21a-112">Anger att cmdleten tvingar bort Application Gateway, oavsett om det är tilldelat resurser eller inte.</span><span class="sxs-lookup"><span data-stu-id="8c21a-112">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="8c21a-113">-Namn</span><span class="sxs-lookup"><span data-stu-id="8c21a-113">-Name</span></span>
<span data-ttu-id="8c21a-114">Anger namnet på den Programgateway som ska tas bort.</span><span class="sxs-lookup"><span data-stu-id="8c21a-114">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="8c21a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c21a-115">-PassThru</span></span>
<span data-ttu-id="8c21a-116">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="8c21a-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8c21a-117">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="8c21a-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8c21a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c21a-118">-ResourceGroupName</span></span>
<span data-ttu-id="8c21a-119">Anger namnet på resurs grupps namnet som applikations-gatewayen tillhör.</span><span class="sxs-lookup"><span data-stu-id="8c21a-119">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="8c21a-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="8c21a-120">-Confirm</span></span>
<span data-ttu-id="8c21a-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="8c21a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c21a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c21a-122">-WhatIf</span></span>
<span data-ttu-id="8c21a-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="8c21a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c21a-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="8c21a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c21a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c21a-125">-DefaultProfile</span></span>
<span data-ttu-id="8c21a-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="8c21a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c21a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c21a-127">CommonParameters</span></span>
<span data-ttu-id="8c21a-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c21a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c21a-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c21a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c21a-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="8c21a-130">INPUTS</span></span>

## <span data-ttu-id="8c21a-131">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="8c21a-131">OUTPUTS</span></span>

### <span data-ttu-id="8c21a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8c21a-132">System.String</span></span>

## <span data-ttu-id="8c21a-133">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="8c21a-133">NOTES</span></span>

## <span data-ttu-id="8c21a-134">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="8c21a-134">RELATED LINKS</span></span>

[<span data-ttu-id="8c21a-135">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="8c21a-135">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)


