---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccount.md
ms.openlocfilehash: ec1e223359c3d83a3cfb77810e0e680f7142bc60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582387"
---
# <span data-ttu-id="e68fe-101">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="e68fe-101">New-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="e68fe-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e68fe-102">SYNOPSIS</span></span>
<span data-ttu-id="e68fe-103">Skapar ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="e68fe-103">Creates an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e68fe-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e68fe-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e68fe-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e68fe-105">DESCRIPTION</span></span>
<span data-ttu-id="e68fe-106">Cmdleten **New-AzureRmIntegrationAccount** skapar ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="e68fe-106">The **New-AzureRmIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="e68fe-107">Denna cmdlet returnerar ett objekt som representerar integrations kontot. Ange ett namn, en plats, resurs gruppens namn och ett SKU-namn.</span><span class="sxs-lookup"><span data-stu-id="e68fe-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>

<span data-ttu-id="e68fe-108">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="e68fe-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="e68fe-109">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="e68fe-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e68fe-110">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="e68fe-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e68fe-111">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="e68fe-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e68fe-112">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="e68fe-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e68fe-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e68fe-113">EXAMPLES</span></span>

### <span data-ttu-id="e68fe-114">Exempel 1: skapa ett integrations konto</span><span class="sxs-lookup"><span data-stu-id="e68fe-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="e68fe-115">Det här kommandot skapar ett integrerings konto med namnet IntegrationAccount31 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e68fe-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="e68fe-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e68fe-116">PARAMETERS</span></span>

### <span data-ttu-id="e68fe-117">-Plats</span><span class="sxs-lookup"><span data-stu-id="e68fe-117">-Location</span></span>
<span data-ttu-id="e68fe-118">Anger en plats för integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="e68fe-118">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="e68fe-119">-Namn</span><span class="sxs-lookup"><span data-stu-id="e68fe-119">-Name</span></span>
<span data-ttu-id="e68fe-120">Anger ett namn på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="e68fe-120">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="e68fe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e68fe-121">-ResourceGroupName</span></span>
<span data-ttu-id="e68fe-122">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="e68fe-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e68fe-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="e68fe-123">-Sku</span></span>
<span data-ttu-id="e68fe-124">Anger ett SKU-namn för integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="e68fe-124">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="e68fe-125">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e68fe-125">-Confirm</span></span>
<span data-ttu-id="e68fe-126">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e68fe-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e68fe-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e68fe-127">-WhatIf</span></span>
<span data-ttu-id="e68fe-128">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e68fe-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e68fe-129">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e68fe-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e68fe-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e68fe-130">-DefaultProfile</span></span>
<span data-ttu-id="e68fe-131">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e68fe-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e68fe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e68fe-132">CommonParameters</span></span>
<span data-ttu-id="e68fe-133">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e68fe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e68fe-134">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e68fe-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e68fe-135">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e68fe-135">INPUTS</span></span>

## <span data-ttu-id="e68fe-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e68fe-136">OUTPUTS</span></span>

### <span data-ttu-id="e68fe-137">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="e68fe-137">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="e68fe-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e68fe-138">NOTES</span></span>

## <span data-ttu-id="e68fe-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e68fe-139">RELATED LINKS</span></span>

[<span data-ttu-id="e68fe-140">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="e68fe-140">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="e68fe-141">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="e68fe-141">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)

[<span data-ttu-id="e68fe-142">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="e68fe-142">Set-AzureRmIntegrationAccount</span></span>](./Set-AzureRmIntegrationAccount.md)


