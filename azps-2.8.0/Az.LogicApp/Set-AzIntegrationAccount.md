---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
ms.openlocfilehash: 8c4c97b1574777a05560f7faa64f0bb4a3476bb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93743744"
---
# <span data-ttu-id="3d0b7-101">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3d0b7-101">Set-AzIntegrationAccount</span></span>

## <span data-ttu-id="3d0b7-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3d0b7-102">SYNOPSIS</span></span>
<span data-ttu-id="3d0b7-103">Ändrar ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="3d0b7-103">Modifies an integration account.</span></span>

## <span data-ttu-id="3d0b7-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3d0b7-104">SYNTAX</span></span>

```
Set-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d0b7-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3d0b7-105">DESCRIPTION</span></span>
<span data-ttu-id="3d0b7-106">Cmdleten **set-AzIntegrationAccount** ändrar ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="3d0b7-106">The **Set-AzIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="3d0b7-107">Denna cmdlet returnerar ett objekt som representerar integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="3d0b7-107">This cmdlet returns an object that represents the integration account.</span></span>
<span data-ttu-id="3d0b7-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="3d0b7-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3d0b7-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="3d0b7-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3d0b7-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="3d0b7-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3d0b7-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="3d0b7-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3d0b7-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3d0b7-112">EXAMPLES</span></span>

### <span data-ttu-id="3d0b7-113">Exempel 1: ändra ett integrations konto</span><span class="sxs-lookup"><span data-stu-id="3d0b7-113">Example 1: Modify an integration account</span></span>
```
PS C:\>Set-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Sku "Free"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="3d0b7-114">Det här kommandot ändrar ett integrerings konto med namnet IntegrationAccount31 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3d0b7-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="3d0b7-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3d0b7-115">PARAMETERS</span></span>

### <span data-ttu-id="3d0b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d0b7-116">-DefaultProfile</span></span>
<span data-ttu-id="3d0b7-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="3d0b7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d0b7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3d0b7-118">-Force</span></span>
<span data-ttu-id="3d0b7-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="3d0b7-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3d0b7-120">-Plats</span><span class="sxs-lookup"><span data-stu-id="3d0b7-120">-Location</span></span>
<span data-ttu-id="3d0b7-121">Anger en plats för integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="3d0b7-121">Specifies a location for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d0b7-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="3d0b7-122">-Name</span></span>
<span data-ttu-id="3d0b7-123">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="3d0b7-123">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d0b7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d0b7-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d0b7-125">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3d0b7-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3d0b7-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="3d0b7-126">-Sku</span></span>
<span data-ttu-id="3d0b7-127">Anger ett SKU-namn för integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="3d0b7-127">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d0b7-128">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="3d0b7-128">-Confirm</span></span>
<span data-ttu-id="3d0b7-129">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="3d0b7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d0b7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d0b7-130">-WhatIf</span></span>
<span data-ttu-id="3d0b7-131">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="3d0b7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d0b7-132">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="3d0b7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d0b7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d0b7-133">CommonParameters</span></span>
<span data-ttu-id="3d0b7-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d0b7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d0b7-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d0b7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d0b7-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3d0b7-136">INPUTS</span></span>

### <span data-ttu-id="3d0b7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3d0b7-137">System.String</span></span>

## <span data-ttu-id="3d0b7-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3d0b7-138">OUTPUTS</span></span>

### <span data-ttu-id="3d0b7-139">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3d0b7-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="3d0b7-140">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3d0b7-140">NOTES</span></span>

## <span data-ttu-id="3d0b7-141">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3d0b7-141">RELATED LINKS</span></span>

[<span data-ttu-id="3d0b7-142">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3d0b7-142">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="3d0b7-143">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3d0b7-143">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="3d0b7-144">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3d0b7-144">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)


