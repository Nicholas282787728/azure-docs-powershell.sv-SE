---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccount.md
ms.openlocfilehash: 3861e4bdc9c61f1e08664f90fd6efbf8ddcedab4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756940"
---
# <span data-ttu-id="cb70b-101">Set-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cb70b-101">Set-AzureRmIntegrationAccount</span></span>

## <span data-ttu-id="cb70b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb70b-102">SYNOPSIS</span></span>
<span data-ttu-id="cb70b-103">Ändrar ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="cb70b-103">Modifies an integration account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb70b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb70b-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb70b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb70b-105">DESCRIPTION</span></span>
<span data-ttu-id="cb70b-106">Cmdleten **set-AzureRmIntegrationAccount** ändrar ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="cb70b-106">The **Set-AzureRmIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="cb70b-107">Denna cmdlet returnerar ett objekt som representerar integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="cb70b-107">This cmdlet returns an object that represents the integration account.</span></span>

<span data-ttu-id="cb70b-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="cb70b-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cb70b-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="cb70b-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cb70b-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="cb70b-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cb70b-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="cb70b-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cb70b-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb70b-112">EXAMPLES</span></span>

### <span data-ttu-id="cb70b-113">Exempel 1: ändra ett integrations konto</span><span class="sxs-lookup"><span data-stu-id="cb70b-113">Example 1: Modify an integration account</span></span>
```
PS C:\>Set-AzureRmIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Sku "Free"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="cb70b-114">Det här kommandot ändrar ett integrerings konto med namnet IntegrationAccount31 i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cb70b-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="cb70b-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb70b-115">PARAMETERS</span></span>

### <span data-ttu-id="cb70b-116">-Force</span><span class="sxs-lookup"><span data-stu-id="cb70b-116">-Force</span></span>
<span data-ttu-id="cb70b-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="cb70b-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cb70b-118">-Plats</span><span class="sxs-lookup"><span data-stu-id="cb70b-118">-Location</span></span>
<span data-ttu-id="cb70b-119">Anger en plats för integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="cb70b-119">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="cb70b-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="cb70b-120">-Name</span></span>
<span data-ttu-id="cb70b-121">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="cb70b-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="cb70b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb70b-122">-ResourceGroupName</span></span>
<span data-ttu-id="cb70b-123">Anger namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="cb70b-123">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cb70b-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="cb70b-124">-Sku</span></span>
<span data-ttu-id="cb70b-125">Anger ett SKU-namn för integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="cb70b-125">Specifies a SKU name for the integration account.</span></span>

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

### <span data-ttu-id="cb70b-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cb70b-126">-Confirm</span></span>
<span data-ttu-id="cb70b-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cb70b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb70b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb70b-128">-WhatIf</span></span>
<span data-ttu-id="cb70b-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cb70b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb70b-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cb70b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb70b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb70b-131">-DefaultProfile</span></span>
<span data-ttu-id="cb70b-132">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb70b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb70b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb70b-133">CommonParameters</span></span>
<span data-ttu-id="cb70b-134">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb70b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb70b-135">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb70b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb70b-136">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb70b-136">INPUTS</span></span>

## <span data-ttu-id="cb70b-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb70b-137">OUTPUTS</span></span>

### <span data-ttu-id="cb70b-138">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cb70b-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="cb70b-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb70b-139">NOTES</span></span>

## <span data-ttu-id="cb70b-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb70b-140">RELATED LINKS</span></span>

[<span data-ttu-id="cb70b-141">Get-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cb70b-141">Get-AzureRmIntegrationAccount</span></span>](./Get-AzureRmIntegrationAccount.md)

[<span data-ttu-id="cb70b-142">New-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cb70b-142">New-AzureRmIntegrationAccount</span></span>](./New-AzureRmIntegrationAccount.md)

[<span data-ttu-id="cb70b-143">Remove-AzureRmIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="cb70b-143">Remove-AzureRmIntegrationAccount</span></span>](./Remove-AzureRmIntegrationAccount.md)


