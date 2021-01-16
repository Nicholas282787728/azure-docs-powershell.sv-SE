---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
ms.openlocfilehash: 50eab845d20d9bf95c20e94f6309be2a302f413c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390417"
---
# <span data-ttu-id="14d0f-101">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="14d0f-101">Remove-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="14d0f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="14d0f-102">SYNOPSIS</span></span>
<span data-ttu-id="14d0f-103">Tar bort ett integrerings konto schema.</span><span class="sxs-lookup"><span data-stu-id="14d0f-103">Removes an integration account schema.</span></span>

## <span data-ttu-id="14d0f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="14d0f-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14d0f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="14d0f-105">DESCRIPTION</span></span>
<span data-ttu-id="14d0f-106">Cmdleten **Remove-AzIntegrationAccountSchema** tar bort ett integrations konto schema från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="14d0f-106">The **Remove-AzIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="14d0f-107">Ange integrerings konto namn, resurs grupps namn och schema namn.</span><span class="sxs-lookup"><span data-stu-id="14d0f-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="14d0f-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="14d0f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="14d0f-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="14d0f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="14d0f-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="14d0f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="14d0f-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="14d0f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="14d0f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="14d0f-112">EXAMPLES</span></span>

### <span data-ttu-id="14d0f-113">Exempel 1: ta bort ett integrations konto schema</span><span class="sxs-lookup"><span data-stu-id="14d0f-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="14d0f-114">Det här kommandot tar bort ett integrerings konto schema med namnet IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="14d0f-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="14d0f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="14d0f-115">PARAMETERS</span></span>

### <span data-ttu-id="14d0f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14d0f-116">-DefaultProfile</span></span>
<span data-ttu-id="14d0f-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="14d0f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14d0f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="14d0f-118">-Force</span></span>
<span data-ttu-id="14d0f-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="14d0f-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="14d0f-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="14d0f-120">-Name</span></span>
<span data-ttu-id="14d0f-121">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="14d0f-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="14d0f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14d0f-122">-ResourceGroupName</span></span>
<span data-ttu-id="14d0f-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="14d0f-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="14d0f-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="14d0f-124">-SchemaName</span></span>
<span data-ttu-id="14d0f-125">Anger namnet på ett integrations konto schema.</span><span class="sxs-lookup"><span data-stu-id="14d0f-125">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="14d0f-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="14d0f-126">-Confirm</span></span>
<span data-ttu-id="14d0f-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="14d0f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14d0f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14d0f-128">-WhatIf</span></span>
<span data-ttu-id="14d0f-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="14d0f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14d0f-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="14d0f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14d0f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14d0f-131">CommonParameters</span></span>
<span data-ttu-id="14d0f-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14d0f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14d0f-133">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14d0f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14d0f-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="14d0f-134">INPUTS</span></span>

### <span data-ttu-id="14d0f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="14d0f-135">System.String</span></span>

## <span data-ttu-id="14d0f-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="14d0f-136">OUTPUTS</span></span>

### <span data-ttu-id="14d0f-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="14d0f-137">System.Void</span></span>

## <span data-ttu-id="14d0f-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="14d0f-138">NOTES</span></span>

## <span data-ttu-id="14d0f-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="14d0f-139">RELATED LINKS</span></span>

[<span data-ttu-id="14d0f-140">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="14d0f-140">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="14d0f-141">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="14d0f-141">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="14d0f-142">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="14d0f-142">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


