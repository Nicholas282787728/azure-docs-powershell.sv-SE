---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountmap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: 769a92f9cd164ef2b3754a84d7a948f3bedd05da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574930"
---
# <span data-ttu-id="4b039-101">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4b039-101">Remove-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="4b039-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4b039-102">SYNOPSIS</span></span>
<span data-ttu-id="4b039-103">Tar bort en integrerings konto karta.</span><span class="sxs-lookup"><span data-stu-id="4b039-103">Removes an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b039-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4b039-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b039-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4b039-105">DESCRIPTION</span></span>
<span data-ttu-id="4b039-106">Cmdleten **Remove-AzureRmIntegrationAccountMap** tar bort en integrerings konto översikt från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="4b039-106">The **Remove-AzureRmIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="4b039-107">Ange integrerings konto namnet, resurs gruppens namn och kartans namn.</span><span class="sxs-lookup"><span data-stu-id="4b039-107">Specify the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="4b039-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="4b039-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4b039-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="4b039-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4b039-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="4b039-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4b039-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="4b039-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4b039-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4b039-112">EXAMPLES</span></span>

### <span data-ttu-id="4b039-113">Exempel 1: ta bort en integrerings konto karta</span><span class="sxs-lookup"><span data-stu-id="4b039-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="4b039-114">Det här kommandot tar bort integrerings konto översikten med namnet IntegrationAccountMap47.</span><span class="sxs-lookup"><span data-stu-id="4b039-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="4b039-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4b039-115">PARAMETERS</span></span>

### <span data-ttu-id="4b039-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b039-116">-DefaultProfile</span></span>
<span data-ttu-id="4b039-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="4b039-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b039-118">-Force</span><span class="sxs-lookup"><span data-stu-id="4b039-118">-Force</span></span>
<span data-ttu-id="4b039-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="4b039-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b039-120">-MapName</span><span class="sxs-lookup"><span data-stu-id="4b039-120">-MapName</span></span>
<span data-ttu-id="4b039-121">Anger namnet på integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="4b039-121">Specifies the name of the integration account map.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b039-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="4b039-122">-Name</span></span>
<span data-ttu-id="4b039-123">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="4b039-123">Specifies the name of the integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b039-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b039-124">-ResourceGroupName</span></span>
<span data-ttu-id="4b039-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="4b039-125">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b039-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4b039-126">-Confirm</span></span>
<span data-ttu-id="4b039-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4b039-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b039-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b039-128">-WhatIf</span></span>
<span data-ttu-id="4b039-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4b039-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b039-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4b039-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b039-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b039-131">CommonParameters</span></span>
<span data-ttu-id="4b039-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b039-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b039-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b039-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b039-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4b039-134">INPUTS</span></span>

### <span data-ttu-id="4b039-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="4b039-135">None</span></span>
<span data-ttu-id="4b039-136">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="4b039-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4b039-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4b039-137">OUTPUTS</span></span>

## <span data-ttu-id="4b039-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4b039-138">NOTES</span></span>

## <span data-ttu-id="4b039-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4b039-139">RELATED LINKS</span></span>

[<span data-ttu-id="4b039-140">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4b039-140">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="4b039-141">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4b039-141">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="4b039-142">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="4b039-142">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)


