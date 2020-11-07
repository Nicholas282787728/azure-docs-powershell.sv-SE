---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7AAF2ACC-84ED-449C-B1E8-F074463F44EB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountMap.md
ms.openlocfilehash: a7104f33fd2e5b9428b062bd8ac359ccabb25520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582379"
---
# <span data-ttu-id="09441-101">Remove-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="09441-101">Remove-AzureRmIntegrationAccountMap</span></span>

## <span data-ttu-id="09441-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="09441-102">SYNOPSIS</span></span>
<span data-ttu-id="09441-103">Tar bort en integrerings konto karta.</span><span class="sxs-lookup"><span data-stu-id="09441-103">Removes an integration account map.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09441-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="09441-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountMap -ResourceGroupName <String> -Name <String> -MapName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09441-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="09441-105">DESCRIPTION</span></span>
<span data-ttu-id="09441-106">Cmdleten **Remove-AzureRmIntegrationAccountMap** tar bort en integrerings konto översikt från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="09441-106">The **Remove-AzureRmIntegrationAccountMap** cmdlet removes an integration account map from a resource group.</span></span>
<span data-ttu-id="09441-107">Ange integrerings konto namnet, resurs gruppens namn och kartans namn.</span><span class="sxs-lookup"><span data-stu-id="09441-107">Specify the integration account name, resource group name, and map name.</span></span>

<span data-ttu-id="09441-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="09441-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="09441-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="09441-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="09441-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="09441-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="09441-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="09441-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="09441-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="09441-112">EXAMPLES</span></span>

### <span data-ttu-id="09441-113">Exempel 1: ta bort en integrerings konto karta</span><span class="sxs-lookup"><span data-stu-id="09441-113">Example 1: Remove an integration account map</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountMap -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -MapName "IntegrationAccountMap47"
```

<span data-ttu-id="09441-114">Det här kommandot tar bort integrerings konto översikten med namnet IntegrationAccountMap47.</span><span class="sxs-lookup"><span data-stu-id="09441-114">This command removes the integration account map named IntegrationAccountMap47.</span></span>

## <span data-ttu-id="09441-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="09441-115">PARAMETERS</span></span>

### <span data-ttu-id="09441-116">-Force</span><span class="sxs-lookup"><span data-stu-id="09441-116">-Force</span></span>
<span data-ttu-id="09441-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="09441-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="09441-118">-MapName</span><span class="sxs-lookup"><span data-stu-id="09441-118">-MapName</span></span>
<span data-ttu-id="09441-119">Anger namnet på integrerings konto översikten.</span><span class="sxs-lookup"><span data-stu-id="09441-119">Specifies the name of the integration account map.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09441-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="09441-120">-Name</span></span>
<span data-ttu-id="09441-121">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="09441-121">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09441-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09441-122">-ResourceGroupName</span></span>
<span data-ttu-id="09441-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="09441-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="09441-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="09441-124">-Confirm</span></span>
<span data-ttu-id="09441-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="09441-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09441-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09441-126">-WhatIf</span></span>
<span data-ttu-id="09441-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="09441-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09441-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="09441-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09441-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09441-129">-DefaultProfile</span></span>
<span data-ttu-id="09441-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="09441-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09441-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09441-131">CommonParameters</span></span>
<span data-ttu-id="09441-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09441-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09441-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09441-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09441-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="09441-134">INPUTS</span></span>

## <span data-ttu-id="09441-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="09441-135">OUTPUTS</span></span>

## <span data-ttu-id="09441-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="09441-136">NOTES</span></span>

## <span data-ttu-id="09441-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="09441-137">RELATED LINKS</span></span>

[<span data-ttu-id="09441-138">Get-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="09441-138">Get-AzureRmIntegrationAccountMap</span></span>](./Get-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="09441-139">New-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="09441-139">New-AzureRmIntegrationAccountMap</span></span>](./New-AzureRmIntegrationAccountMap.md)

[<span data-ttu-id="09441-140">Set-AzureRmIntegrationAccountMap</span><span class="sxs-lookup"><span data-stu-id="09441-140">Set-AzureRmIntegrationAccountMap</span></span>](./Set-AzureRmIntegrationAccountMap.md)

