---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: b002ca0dca3f3974af8cd05e8ae7c7babf2af486
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93584192"
---
# <span data-ttu-id="f4d49-101">Set-AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="f4d49-101">Set-AzureRmIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="f4d49-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="f4d49-102">SYNOPSIS</span></span>
<span data-ttu-id="f4d49-103">Uppdaterar integrerings kontots genererade utbytes kontroll nummer (ICN) i Azure-resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="f4d49-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4d49-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="f4d49-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4d49-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="f4d49-105">DESCRIPTION</span></span>
<span data-ttu-id="f4d49-106">Set-AzureRmIntegrationAccountGeneratedIcn cmdlet uppdaterar ett befintligt integrerings konto som genererade utbytes kontroll nummer (ICN) och returnerar ett objekt som representerar integrerings kontots genererade kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="f4d49-106">The Set-AzureRmIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="f4d49-107">Använd denna cmdlet för att uppdatera ett integrerings konto som genererat överförings kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="f4d49-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="f4d49-108">Du kan uppdatera ett integrerings konto som genererade utbytes kontroll nummer genom att ange integrerings konto namn, resurs grupp namn och avtals namn.</span><span class="sxs-lookup"><span data-stu-id="f4d49-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="f4d49-109">Du kan inte skapa ett nytt integrerings konto som genererat överförings kontroll nummer med det här kommandot.</span><span class="sxs-lookup"><span data-stu-id="f4d49-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="f4d49-110">Om du vill använda de dynamiska parametrarna skriver du bara in dem i kommandot eller skriver ett bindestreck (-) för att ange ett parameter namn och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="f4d49-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f4d49-111">Om du missar en obligatorisk mallparameter ber cmdleten dig om värdet.</span><span class="sxs-lookup"><span data-stu-id="f4d49-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="f4d49-112">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="f4d49-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="f4d49-113">Ange om X12-eller EDIFACT kontroll nummer ska returneras med parametern "-AgreementType".</span><span class="sxs-lookup"><span data-stu-id="f4d49-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="f4d49-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="f4d49-114">EXAMPLES</span></span>

### <span data-ttu-id="f4d49-115">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="f4d49-115">Example 1</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "X12IntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType X12 -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="f4d49-116">Det här kommandot får integrerings kontot som genererat X12 Interchange Control-nummer för ett specifikt integrerings konto avtal, öka värdet med 100 och skriver sedan tillbaka det uppdaterade värdet.</span><span class="sxs-lookup"><span data-stu-id="f4d49-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="f4d49-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="f4d49-117">Example 2</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "EdifactIntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType EdifactIntegrationAccountAgreement -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="f4d49-118">Det här kommandot får integrerings kontot som genererat EdifactIntegrationAccountAgreement Interchange Control-nummer för ett specifikt integrerings konto avtal, öka värdet med 100 och skriver sedan tillbaka det uppdaterade värdet.</span><span class="sxs-lookup"><span data-stu-id="f4d49-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="f4d49-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="f4d49-119">PARAMETERS</span></span>

### <span data-ttu-id="f4d49-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="f4d49-120">-AgreementName</span></span>
<span data-ttu-id="f4d49-121">Namnet på integrerings konto avtalet.</span><span class="sxs-lookup"><span data-stu-id="f4d49-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="f4d49-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="f4d49-122">-AgreementType</span></span>
<span data-ttu-id="f4d49-123">Avtals typen integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="f4d49-123">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4d49-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="f4d49-124">-ControlNumber</span></span>
<span data-ttu-id="f4d49-125">Det nya värdet för kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="f4d49-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="f4d49-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4d49-126">-DefaultProfile</span></span>
<span data-ttu-id="f4d49-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="f4d49-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4d49-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="f4d49-128">-Name</span></span>
<span data-ttu-id="f4d49-129">Namn på integrations konto.</span><span class="sxs-lookup"><span data-stu-id="f4d49-129">The integration account name.</span></span>

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

### <span data-ttu-id="f4d49-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4d49-130">-ResourceGroupName</span></span>
<span data-ttu-id="f4d49-131">Namnet på integrations konto resursen.</span><span class="sxs-lookup"><span data-stu-id="f4d49-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="f4d49-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="f4d49-132">-Confirm</span></span>
<span data-ttu-id="f4d49-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="f4d49-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4d49-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4d49-134">-WhatIf</span></span>
<span data-ttu-id="f4d49-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="f4d49-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4d49-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="f4d49-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4d49-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4d49-137">CommonParameters</span></span>
<span data-ttu-id="f4d49-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4d49-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4d49-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4d49-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4d49-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="f4d49-140">INPUTS</span></span>

### <span data-ttu-id="f4d49-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f4d49-141">System.String</span></span>

## <span data-ttu-id="f4d49-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="f4d49-142">OUTPUTS</span></span>

### <span data-ttu-id="f4d49-143">Microsoft. Azure. commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="f4d49-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="f4d49-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="f4d49-144">NOTES</span></span>

## <span data-ttu-id="f4d49-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="f4d49-145">RELATED LINKS</span></span>

[<span data-ttu-id="f4d49-146">Get-AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="f4d49-146">Get-AzureRmIntegrationAccountGeneratedIcn</span></span>](./Get-AzureRmIntegrationAccountGeneratedIcn.md)

