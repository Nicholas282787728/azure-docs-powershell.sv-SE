---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 39D1576D-7042-4A62-AB41-0B5131C150D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmLogicApp.md
ms.openlocfilehash: 3650e04b8c6d254b396072c55d39cde38a1328f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93579484"
---
# <span data-ttu-id="ba305-101">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba305-101">Remove-AzureRmLogicApp</span></span>

## <span data-ttu-id="ba305-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ba305-102">SYNOPSIS</span></span>
<span data-ttu-id="ba305-103">Tar bort ett logiskt program från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ba305-103">Removes a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba305-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ba305-104">SYNTAX</span></span>

```
Remove-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba305-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ba305-105">DESCRIPTION</span></span>
<span data-ttu-id="ba305-106">Med cmdleten **Remove-AzureRmLogicApp** tar du bort ett logiskt program från en resurs grupp med hjälp av funktionen logiska appar.</span><span class="sxs-lookup"><span data-stu-id="ba305-106">The **Remove-AzureRmLogicApp** cmdlet removes a logic app from a resource group by using the Logic Apps feature.</span></span>
<span data-ttu-id="ba305-107">Ange logik programmet och resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="ba305-107">Specify the logic app and resource group.</span></span>

<span data-ttu-id="ba305-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="ba305-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ba305-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="ba305-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ba305-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="ba305-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ba305-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="ba305-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ba305-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ba305-112">EXAMPLES</span></span>

### <span data-ttu-id="ba305-113">Exempel 1: ta bort ett logik program</span><span class="sxs-lookup"><span data-stu-id="ba305-113">Example 1: Remove a logic app</span></span>
```
PS C:\>Remove-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03" -Force
```

<span data-ttu-id="ba305-114">Det här kommandot tar bort ett logiskt program från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="ba305-114">This command removes a logic app from a resource group.</span></span>
<span data-ttu-id="ba305-115">Kommandot innehåller parametern *Force* , som hindrar kommandot från att bekräfta.</span><span class="sxs-lookup"><span data-stu-id="ba305-115">The command includes the *Force* parameter, which prevents the command from prompting you for confirmation.</span></span>

## <span data-ttu-id="ba305-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ba305-116">PARAMETERS</span></span>

### <span data-ttu-id="ba305-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba305-117">-DefaultProfile</span></span>
<span data-ttu-id="ba305-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ba305-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ba305-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ba305-119">-Force</span></span>
<span data-ttu-id="ba305-120">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="ba305-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ba305-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="ba305-121">-Name</span></span>
<span data-ttu-id="ba305-122">Anger namnet på det logik program som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="ba305-122">Specifies the name of the logic app that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba305-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba305-123">-ResourceGroupName</span></span>
<span data-ttu-id="ba305-124">Anger namnet på den resurs grupp som innehåller det logik program som den här cmdleten tar bort.</span><span class="sxs-lookup"><span data-stu-id="ba305-124">Specifies the name of the resource group that contains the logic app that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ba305-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ba305-125">-Confirm</span></span>
<span data-ttu-id="ba305-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ba305-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba305-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba305-127">-WhatIf</span></span>
<span data-ttu-id="ba305-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ba305-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba305-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ba305-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba305-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba305-130">CommonParameters</span></span>
<span data-ttu-id="ba305-131">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba305-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba305-132">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba305-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba305-133">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ba305-133">INPUTS</span></span>

### <span data-ttu-id="ba305-134">Ingen</span><span class="sxs-lookup"><span data-stu-id="ba305-134">None</span></span>
<span data-ttu-id="ba305-135">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="ba305-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ba305-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ba305-136">OUTPUTS</span></span>

### <span data-ttu-id="ba305-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="ba305-137">System.Object</span></span>

## <span data-ttu-id="ba305-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ba305-138">NOTES</span></span>

## <span data-ttu-id="ba305-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ba305-139">RELATED LINKS</span></span>

[<span data-ttu-id="ba305-140">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba305-140">Get-AzureRmLogicApp</span></span>](./Get-AzureRmLogicApp.md)

[<span data-ttu-id="ba305-141">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba305-141">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="ba305-142">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba305-142">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="ba305-143">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="ba305-143">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


