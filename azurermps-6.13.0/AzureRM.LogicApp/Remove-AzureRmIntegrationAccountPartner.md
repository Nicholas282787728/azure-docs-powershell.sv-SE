---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 9268d1859f42b7849f8e4a61ae39aa4b68994e4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93577987"
---
# <span data-ttu-id="6f6fb-101">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="6f6fb-101">Remove-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="6f6fb-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6f6fb-102">SYNOPSIS</span></span>
<span data-ttu-id="6f6fb-103">Tar bort en integrerings konto partner.</span><span class="sxs-lookup"><span data-stu-id="6f6fb-103">Removes an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f6fb-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6f6fb-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f6fb-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6f6fb-105">DESCRIPTION</span></span>
<span data-ttu-id="6f6fb-106">Cmdleten **Remove-AzureRmIntegrationAccountPartner** tar bort en integrerings konto partner från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6f6fb-106">The **Remove-AzureRmIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="6f6fb-107">Ange integrerings konto namn, resurs grupps namn och partner namn.</span><span class="sxs-lookup"><span data-stu-id="6f6fb-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="6f6fb-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="6f6fb-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6f6fb-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="6f6fb-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6f6fb-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="6f6fb-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6f6fb-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="6f6fb-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6f6fb-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6f6fb-112">EXAMPLES</span></span>

### <span data-ttu-id="6f6fb-113">Exempel 1: ta bort en integrerings konto partner</span><span class="sxs-lookup"><span data-stu-id="6f6fb-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="6f6fb-114">Det här kommandot tar bort integrerings konto partnern med namnet IntegrationAccountPartner1.</span><span class="sxs-lookup"><span data-stu-id="6f6fb-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="6f6fb-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6f6fb-115">PARAMETERS</span></span>

### <span data-ttu-id="6f6fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f6fb-116">-DefaultProfile</span></span>
<span data-ttu-id="6f6fb-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6f6fb-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f6fb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6f6fb-118">-Force</span></span>
<span data-ttu-id="6f6fb-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6f6fb-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6f6fb-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="6f6fb-120">-Name</span></span>
<span data-ttu-id="6f6fb-121">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="6f6fb-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="6f6fb-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="6f6fb-122">-PartnerName</span></span>
<span data-ttu-id="6f6fb-123">Anger namnet på integrations konto partnern.</span><span class="sxs-lookup"><span data-stu-id="6f6fb-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="6f6fb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f6fb-124">-ResourceGroupName</span></span>
<span data-ttu-id="6f6fb-125">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6f6fb-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6f6fb-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6f6fb-126">-Confirm</span></span>
<span data-ttu-id="6f6fb-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6f6fb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f6fb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f6fb-128">-WhatIf</span></span>
<span data-ttu-id="6f6fb-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6f6fb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f6fb-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6f6fb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f6fb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f6fb-131">CommonParameters</span></span>
<span data-ttu-id="6f6fb-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f6fb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f6fb-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f6fb-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f6fb-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6f6fb-134">INPUTS</span></span>

### <span data-ttu-id="6f6fb-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6f6fb-135">System.String</span></span>

## <span data-ttu-id="6f6fb-136">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6f6fb-136">OUTPUTS</span></span>

### <span data-ttu-id="6f6fb-137">System. Void</span><span class="sxs-lookup"><span data-stu-id="6f6fb-137">System.Void</span></span>

## <span data-ttu-id="6f6fb-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6f6fb-138">NOTES</span></span>

## <span data-ttu-id="6f6fb-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6f6fb-139">RELATED LINKS</span></span>

[<span data-ttu-id="6f6fb-140">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="6f6fb-140">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="6f6fb-141">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="6f6fb-141">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="6f6fb-142">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="6f6fb-142">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


