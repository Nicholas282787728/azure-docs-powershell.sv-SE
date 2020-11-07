---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: fbbc071b9c83336a1835f1495d171f7a2414199a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93756933"
---
# <span data-ttu-id="2ec26-101">Set-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="2ec26-101">Set-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="2ec26-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2ec26-102">SYNOPSIS</span></span>
<span data-ttu-id="2ec26-103">Uppdaterar integrerings kontots mottagna utbytes kontroll nummer (ICN) i Azure-resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2ec26-103">Updates the integration account received interchange control number (ICN) in the Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ec26-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2ec26-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ec26-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2ec26-105">DESCRIPTION</span></span>
<span data-ttu-id="2ec26-106">Set-AzureRmIntegrationAccountGeneratedIcn cmdlet uppdaterar ett befintligt integrerings konto som tagits emot Interchange Control Number (ICN) och returnerar ett objekt som representerar integrerings kontots mottagna utbytes kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="2ec26-106">The Set-AzureRmIntegrationAccountGeneratedIcn cmdlet updates an existing integration account received interchange control number (ICN) and returns an object that represents the integration account received interchange control number.</span></span>
<span data-ttu-id="2ec26-107">Använd denna cmdlet för att uppdatera ett integrerings konto som status för överförings kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="2ec26-107">Use this cmdlet to update an integration account received interchange control number's message processing status.</span></span>
<span data-ttu-id="2ec26-108">Du kan uppdatera ett integrerings konto som har fått ett utbytes kontroll nummer genom att ange integrerings konto namn, resurs grupp namn, avtals namn, kontroll nummer och meddelande status.</span><span class="sxs-lookup"><span data-stu-id="2ec26-108">You can update an integration account received interchange control number by specifying the integration account name, resource group name, agreement name, control number value and message processing status.</span></span>
<span data-ttu-id="2ec26-109">Du kan inte skapa ett nytt integrerings konto för utbytes kontroll nummer med det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="2ec26-109">You cannot create a new integration account received interchange control number with this command.</span></span>
<span data-ttu-id="2ec26-110">Om du vill använda de dynamiska parametrarna skriver du bara in dem i kommandot eller skriver ett bindestreck (-) för att ange ett parameter namn och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="2ec26-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2ec26-111">Om du missar en obligatorisk mallparameter ber cmdleten dig om värdet.</span><span class="sxs-lookup"><span data-stu-id="2ec26-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="2ec26-112">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="2ec26-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="2ec26-113">Ange om X12-eller EDIFACT kontroll nummer ska returneras med parametern "-AgreementType".</span><span class="sxs-lookup"><span data-stu-id="2ec26-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="2ec26-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2ec26-114">EXAMPLES</span></span>

### <span data-ttu-id="2ec26-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2ec26-115">Example 1</span></span>
```
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="2ec26-116">Det här kommandot uppdaterar integrerings kontot med X12 Interchange Control-nummer för ett specifikt integrerings konto avtal och ett visst värde för meddelande behandling.</span><span class="sxs-lookup"><span data-stu-id="2ec26-116">This command updates the integration account received X12 interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

### <span data-ttu-id="2ec26-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="2ec26-117">Example 2</span></span>
```
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="2ec26-118">Det här kommandot uppdaterar integrerings kontot med EDIFACT Interchange Control-nummer för ett specifikt integrerings konto avtal och ett visst värde för meddelande behandling.</span><span class="sxs-lookup"><span data-stu-id="2ec26-118">This command updates the integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

## <span data-ttu-id="2ec26-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2ec26-119">PARAMETERS</span></span>

### <span data-ttu-id="2ec26-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="2ec26-120">-AgreementName</span></span>
<span data-ttu-id="2ec26-121">Namnet på integrerings konto avtalet.</span><span class="sxs-lookup"><span data-stu-id="2ec26-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="2ec26-122">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="2ec26-122">-ControlNumberValue</span></span>
<span data-ttu-id="2ec26-123">Värdet på integrations kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="2ec26-123">The integration account control number value.</span></span>

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

### <span data-ttu-id="2ec26-124">-IsMessageProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="2ec26-124">-IsMessageProcessingFailed</span></span>
<span data-ttu-id="2ec26-125">Statusen för mottagen meddelande behandling.</span><span class="sxs-lookup"><span data-stu-id="2ec26-125">The received message processing status.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec26-126">-Namn</span><span class="sxs-lookup"><span data-stu-id="2ec26-126">-Name</span></span>
<span data-ttu-id="2ec26-127">Namn på integrations konto.</span><span class="sxs-lookup"><span data-stu-id="2ec26-127">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec26-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ec26-128">-ResourceGroupName</span></span>
<span data-ttu-id="2ec26-129">Namnet på integrations konto resursen.</span><span class="sxs-lookup"><span data-stu-id="2ec26-129">The integration account resource group name.</span></span>

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

### <span data-ttu-id="2ec26-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="2ec26-130">-Confirm</span></span>
<span data-ttu-id="2ec26-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="2ec26-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ec26-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ec26-132">-WhatIf</span></span>
<span data-ttu-id="2ec26-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="2ec26-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ec26-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="2ec26-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ec26-135">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="2ec26-135">-AgreementType</span></span>
<span data-ttu-id="2ec26-136">Avtals typen integrerings konto (X12 eller EDIFACT).</span><span class="sxs-lookup"><span data-stu-id="2ec26-136">The integration account agreement type (X12 or Edifact).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ec26-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ec26-137">-DefaultProfile</span></span>
<span data-ttu-id="2ec26-138">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2ec26-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ec26-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ec26-139">CommonParameters</span></span>
<span data-ttu-id="2ec26-140">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ec26-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ec26-141">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ec26-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ec26-142">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2ec26-142">INPUTS</span></span>

### <span data-ttu-id="2ec26-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2ec26-143">System.String</span></span>

## <span data-ttu-id="2ec26-144">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2ec26-144">OUTPUTS</span></span>

### <span data-ttu-id="2ec26-145">Microsoft. Azure. commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="2ec26-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="2ec26-146">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2ec26-146">NOTES</span></span>

## <span data-ttu-id="2ec26-147">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2ec26-147">RELATED LINKS</span></span>

<span data-ttu-id="2ec26-148">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md) 
 [Remove-AzureRmIntegrationAccountReceivedIcn](./Remove-AzureRmIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="2ec26-148">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md)
[Remove-AzureRmIntegrationAccountReceivedIcn](./Remove-AzureRmIntegrationAccountReceivedIcn.md)</span></span>
