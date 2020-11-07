---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountSchema.md
ms.openlocfilehash: a1a34ca669b12ee815655531c33b6cdba519016c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757934"
---
# <span data-ttu-id="9904a-101">Remove-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9904a-101">Remove-AzureRmIntegrationAccountSchema</span></span>

## <span data-ttu-id="9904a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="9904a-102">SYNOPSIS</span></span>
<span data-ttu-id="9904a-103">Tar bort ett integrerings konto schema.</span><span class="sxs-lookup"><span data-stu-id="9904a-103">Removes an integration account schema.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9904a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="9904a-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9904a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="9904a-105">DESCRIPTION</span></span>
<span data-ttu-id="9904a-106">Cmdleten **Remove-AzureRmIntegrationAccountSchema** tar bort ett integrations konto schema från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9904a-106">The **Remove-AzureRmIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="9904a-107">Ange integrerings konto namn, resurs grupps namn och schema namn.</span><span class="sxs-lookup"><span data-stu-id="9904a-107">Specifying the integration account name, resource group name, and schema name.</span></span>

<span data-ttu-id="9904a-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="9904a-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9904a-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="9904a-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9904a-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="9904a-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9904a-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="9904a-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9904a-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="9904a-112">EXAMPLES</span></span>

### <span data-ttu-id="9904a-113">Exempel 1: ta bort ett integrations konto schema</span><span class="sxs-lookup"><span data-stu-id="9904a-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="9904a-114">Det här kommandot tar bort ett integrerings konto schema med namnet IntegrationAccountSchema43.</span><span class="sxs-lookup"><span data-stu-id="9904a-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="9904a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="9904a-115">PARAMETERS</span></span>

### <span data-ttu-id="9904a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9904a-116">-DefaultProfile</span></span>
<span data-ttu-id="9904a-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="9904a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9904a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9904a-118">-Force</span></span>
<span data-ttu-id="9904a-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="9904a-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9904a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="9904a-120">-Name</span></span>
<span data-ttu-id="9904a-121">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="9904a-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="9904a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9904a-122">-ResourceGroupName</span></span>
<span data-ttu-id="9904a-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="9904a-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9904a-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="9904a-124">-SchemaName</span></span>
<span data-ttu-id="9904a-125">Anger namnet på ett integrations konto schema.</span><span class="sxs-lookup"><span data-stu-id="9904a-125">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="9904a-126">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="9904a-126">-Confirm</span></span>
<span data-ttu-id="9904a-127">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="9904a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9904a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9904a-128">-WhatIf</span></span>
<span data-ttu-id="9904a-129">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="9904a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9904a-130">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="9904a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9904a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9904a-131">CommonParameters</span></span>
<span data-ttu-id="9904a-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9904a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9904a-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9904a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9904a-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="9904a-134">INPUTS</span></span>

### <span data-ttu-id="9904a-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="9904a-135">None</span></span>
<span data-ttu-id="9904a-136">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="9904a-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9904a-137">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="9904a-137">OUTPUTS</span></span>

## <span data-ttu-id="9904a-138">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="9904a-138">NOTES</span></span>

## <span data-ttu-id="9904a-139">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="9904a-139">RELATED LINKS</span></span>

[<span data-ttu-id="9904a-140">Get-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9904a-140">Get-AzureRmIntegrationAccountSchema</span></span>](./Get-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="9904a-141">New-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9904a-141">New-AzureRmIntegrationAccountSchema</span></span>](./New-AzureRmIntegrationAccountSchema.md)

[<span data-ttu-id="9904a-142">Set-AzureRmIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="9904a-142">Set-AzureRmIntegrationAccountSchema</span></span>](./Set-AzureRmIntegrationAccountSchema.md)


