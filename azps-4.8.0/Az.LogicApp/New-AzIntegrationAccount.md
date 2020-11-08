---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
ms.openlocfilehash: a3a3fc16b253235da82626ab6d827d074f05860d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94101436"
---
# <span data-ttu-id="431fb-101">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="431fb-101">New-AzIntegrationAccount</span></span>

## <span data-ttu-id="431fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="431fb-102">SYNOPSIS</span></span>
<span data-ttu-id="431fb-103">Skapar ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="431fb-103">Creates an integration account.</span></span>

## <span data-ttu-id="431fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="431fb-104">SYNTAX</span></span>

```
New-AzIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="431fb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="431fb-105">DESCRIPTION</span></span>
<span data-ttu-id="431fb-106">Cmdleten **New-AzIntegrationAccount** skapar ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="431fb-106">The **New-AzIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="431fb-107">Denna cmdlet returnerar ett objekt som representerar integrations kontot. Ange ett namn, en plats, resurs gruppens namn och ett SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="431fb-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>
<span data-ttu-id="431fb-108">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="431fb-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="431fb-109">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="431fb-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="431fb-110">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="431fb-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="431fb-111">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="431fb-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="431fb-112">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="431fb-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="431fb-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="431fb-113">EXAMPLES</span></span>

### <span data-ttu-id="431fb-114">Exempel 1: skapa ett integrations konto</span><span class="sxs-lookup"><span data-stu-id="431fb-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="431fb-115">Det här kommandot skapar ett integrerings konto med namnet IntegrationAccount31 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="431fb-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="431fb-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="431fb-116">PARAMETERS</span></span>

### <span data-ttu-id="431fb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="431fb-117">-DefaultProfile</span></span>
<span data-ttu-id="431fb-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="431fb-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="431fb-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="431fb-119">-Location</span></span>
<span data-ttu-id="431fb-120">Anger en plats för integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="431fb-120">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="431fb-121">-Namn</span><span class="sxs-lookup"><span data-stu-id="431fb-121">-Name</span></span>
<span data-ttu-id="431fb-122">Anger ett namn på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="431fb-122">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="431fb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="431fb-123">-ResourceGroupName</span></span>
<span data-ttu-id="431fb-124">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="431fb-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="431fb-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="431fb-125">-Sku</span></span>
<span data-ttu-id="431fb-126">Anger ett SKU-namn för integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="431fb-126">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="431fb-127">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="431fb-127">-Confirm</span></span>
<span data-ttu-id="431fb-128">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="431fb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="431fb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="431fb-129">-WhatIf</span></span>
<span data-ttu-id="431fb-130">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="431fb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="431fb-131">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="431fb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="431fb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="431fb-132">CommonParameters</span></span>
<span data-ttu-id="431fb-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="431fb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="431fb-134">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="431fb-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="431fb-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="431fb-135">INPUTS</span></span>

### <span data-ttu-id="431fb-136">System. String</span><span class="sxs-lookup"><span data-stu-id="431fb-136">System.String</span></span>

## <span data-ttu-id="431fb-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="431fb-137">OUTPUTS</span></span>

### <span data-ttu-id="431fb-138">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="431fb-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="431fb-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="431fb-139">NOTES</span></span>

## <span data-ttu-id="431fb-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="431fb-140">RELATED LINKS</span></span>

[<span data-ttu-id="431fb-141">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="431fb-141">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="431fb-142">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="431fb-142">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="431fb-143">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="431fb-143">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


