---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 4f9beaec4a665871db8bf5dc089deb02617ee8fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93576493"
---
# <span data-ttu-id="d0f64-101">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="d0f64-101">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="d0f64-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d0f64-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f64-103">Denna cmdlet tar bort ett specifikt nummer för utbytes kontroll per avtal och kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="d0f64-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0f64-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d0f64-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0f64-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d0f64-105">DESCRIPTION</span></span>
<span data-ttu-id="d0f64-106">Denna cmdlet är avsedd att användas vid katastrof återställning för att ta bort ett mottaget utbytes nummer från integrerings kontot så att B2B-anslutningen kan bearbeta meddelandet igen när dubblettidentifiering är aktiverat.</span><span class="sxs-lookup"><span data-stu-id="d0f64-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="d0f64-107">I sällsynta fall kan mottagnings kontroll numret reserveras strax före en katastrof och innan B2B-anslutningen avvisar att växlingen är felaktig.</span><span class="sxs-lookup"><span data-stu-id="d0f64-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="d0f64-108">I sådana fall kan det vara bra att aktivera återställnings webbplatsen och bearbeta den igen efter att dess nytto Last har åtgärd ATS.</span><span class="sxs-lookup"><span data-stu-id="d0f64-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="d0f64-109">Ange om X12-eller EDIFACT kontroll nummer ska returneras med parametern "-AgreementType".</span><span class="sxs-lookup"><span data-stu-id="d0f64-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="d0f64-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d0f64-110">EXAMPLES</span></span>

### <span data-ttu-id="d0f64-111">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="d0f64-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The existing recevied control number '000000641' for agreement 'X12AgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The session 'X12-ICN-X12AgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="d0f64-112">Försöker skaffa ett mottaget X12 Interchange Control-nummer som har ett ogiltigt format.</span><span class="sxs-lookup"><span data-stu-id="d0f64-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="d0f64-113">Tar bort det mottagna X12 Interchange Control-numret.</span><span class="sxs-lookup"><span data-stu-id="d0f64-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="d0f64-114">Bekräftar att mottagnings kontroll numret för X12 har tagits bort genom att försöka skaffa det igen.</span><span class="sxs-lookup"><span data-stu-id="d0f64-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="d0f64-115">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d0f64-115">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The existing recevied control number '000000641' for agreement 'EdifactAgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The session 'Edifact-ICN-EdifactAgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="d0f64-116">Försöker skaffa ett mottaget EDIFACT Interchange Control-nummer som har ett ogiltigt format.</span><span class="sxs-lookup"><span data-stu-id="d0f64-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="d0f64-117">Tar bort det mottagna EDIFACT Interchange Control-numret.</span><span class="sxs-lookup"><span data-stu-id="d0f64-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="d0f64-118">Bekräftar att mottagnings kontroll numret för EDIFACT har tagits bort genom att försöka skaffa det igen.</span><span class="sxs-lookup"><span data-stu-id="d0f64-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="d0f64-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d0f64-119">PARAMETERS</span></span>

### <span data-ttu-id="d0f64-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="d0f64-120">-AgreementName</span></span>
<span data-ttu-id="d0f64-121">Namnet på integrerings konto avtalet.</span><span class="sxs-lookup"><span data-stu-id="d0f64-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="d0f64-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="d0f64-122">-AgreementType</span></span>
<span data-ttu-id="d0f64-123">Avtals typen integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="d0f64-123">The integration account agreement type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0f64-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="d0f64-124">-ControlNumberValue</span></span>
<span data-ttu-id="d0f64-125">Värdet på integrations kontroll nummer.</span><span class="sxs-lookup"><span data-stu-id="d0f64-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="d0f64-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f64-126">-DefaultProfile</span></span>
<span data-ttu-id="d0f64-127">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d0f64-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0f64-128">-Namn</span><span class="sxs-lookup"><span data-stu-id="d0f64-128">-Name</span></span>
<span data-ttu-id="d0f64-129">Namn på integrations konto.</span><span class="sxs-lookup"><span data-stu-id="d0f64-129">The integration account name.</span></span>

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

### <span data-ttu-id="d0f64-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0f64-130">-ResourceGroupName</span></span>
<span data-ttu-id="d0f64-131">Namnet på integrations konto resursen.</span><span class="sxs-lookup"><span data-stu-id="d0f64-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="d0f64-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d0f64-132">-Confirm</span></span>
<span data-ttu-id="d0f64-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d0f64-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0f64-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0f64-134">-WhatIf</span></span>
<span data-ttu-id="d0f64-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d0f64-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0f64-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d0f64-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0f64-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f64-137">CommonParameters</span></span>
<span data-ttu-id="d0f64-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0f64-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f64-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0f64-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f64-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d0f64-140">INPUTS</span></span>

### <span data-ttu-id="d0f64-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d0f64-141">System.String</span></span>

## <span data-ttu-id="d0f64-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d0f64-142">OUTPUTS</span></span>

### <span data-ttu-id="d0f64-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="d0f64-143">System.Object</span></span>

## <span data-ttu-id="d0f64-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d0f64-144">NOTES</span></span>

## <span data-ttu-id="d0f64-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d0f64-145">RELATED LINKS</span></span>

<span data-ttu-id="d0f64-146">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md) 
 [Set-AzureRmIntegrationAccountReceivedIcn](./Set-AzureRmIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="d0f64-146">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md)
[Set-AzureRmIntegrationAccountReceivedIcn](./Set-AzureRmIntegrationAccountReceivedIcn.md)</span></span>

