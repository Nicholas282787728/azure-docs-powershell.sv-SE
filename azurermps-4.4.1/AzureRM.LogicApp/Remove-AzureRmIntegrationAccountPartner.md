---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: f10173dce7b64ccc656e2c852c6eb20230d1a7bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582376"
---
# <span data-ttu-id="cb40f-101">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="cb40f-101">Remove-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="cb40f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cb40f-102">SYNOPSIS</span></span>
<span data-ttu-id="cb40f-103">Tar bort en integrerings konto partner.</span><span class="sxs-lookup"><span data-stu-id="cb40f-103">Removes an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb40f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cb40f-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb40f-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cb40f-105">DESCRIPTION</span></span>
<span data-ttu-id="cb40f-106">Cmdleten **Remove-AzureRmIntegrationAccountPartner** tar bort en integrerings konto partner från en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cb40f-106">The **Remove-AzureRmIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="cb40f-107">Ange integrerings konto namn, resurs grupps namn och partner namn.</span><span class="sxs-lookup"><span data-stu-id="cb40f-107">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="cb40f-108">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="cb40f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cb40f-109">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="cb40f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cb40f-110">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="cb40f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cb40f-111">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="cb40f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cb40f-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cb40f-112">EXAMPLES</span></span>

### <span data-ttu-id="cb40f-113">Exempel 1: ta bort en integrerings konto partner</span><span class="sxs-lookup"><span data-stu-id="cb40f-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="cb40f-114">Det här kommandot tar bort integrerings konto partnern med namnet IntegrationAccountPartner1.</span><span class="sxs-lookup"><span data-stu-id="cb40f-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="cb40f-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cb40f-115">PARAMETERS</span></span>

### <span data-ttu-id="cb40f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="cb40f-116">-Force</span></span>
<span data-ttu-id="cb40f-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="cb40f-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cb40f-118">-Namn</span><span class="sxs-lookup"><span data-stu-id="cb40f-118">-Name</span></span>
<span data-ttu-id="cb40f-119">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="cb40f-119">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="cb40f-120">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="cb40f-120">-PartnerName</span></span>
<span data-ttu-id="cb40f-121">Anger namnet på integrations konto partnern.</span><span class="sxs-lookup"><span data-stu-id="cb40f-121">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="cb40f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb40f-122">-ResourceGroupName</span></span>
<span data-ttu-id="cb40f-123">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="cb40f-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cb40f-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cb40f-124">-Confirm</span></span>
<span data-ttu-id="cb40f-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cb40f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb40f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb40f-126">-WhatIf</span></span>
<span data-ttu-id="cb40f-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cb40f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb40f-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cb40f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb40f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb40f-129">-DefaultProfile</span></span>
<span data-ttu-id="cb40f-130">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="cb40f-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb40f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb40f-131">CommonParameters</span></span>
<span data-ttu-id="cb40f-132">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb40f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb40f-133">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb40f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb40f-134">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cb40f-134">INPUTS</span></span>

## <span data-ttu-id="cb40f-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cb40f-135">OUTPUTS</span></span>

## <span data-ttu-id="cb40f-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cb40f-136">NOTES</span></span>

## <span data-ttu-id="cb40f-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cb40f-137">RELATED LINKS</span></span>

[<span data-ttu-id="cb40f-138">Get-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="cb40f-138">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="cb40f-139">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="cb40f-139">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="cb40f-140">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="cb40f-140">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


