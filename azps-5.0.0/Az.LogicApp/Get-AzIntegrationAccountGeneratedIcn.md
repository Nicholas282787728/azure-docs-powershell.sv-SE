---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 0dffb7a99e29ea4cc595cad1b5b92450e83289f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94271885"
---
# <span data-ttu-id="31779-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="31779-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="31779-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="31779-102">SYNOPSIS</span></span>
<span data-ttu-id="31779-103">Denna cmdlet hämtar det aktuella värdet för det genererade utbytes kontroll numret per avtal.</span><span class="sxs-lookup"><span data-stu-id="31779-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="31779-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="31779-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31779-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="31779-105">DESCRIPTION</span></span>
<span data-ttu-id="31779-106">Denna cmdlet är avsedd att användas vid katastrof återställning för att hämta det aktuella värdet för det genererade utbytes kontroll numret så att du kan skriva tillbaka ett ökat värde med set-AzIntegrationAccountGeneratedIcn.</span><span class="sxs-lookup"><span data-stu-id="31779-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="31779-107">Utbytes kontroll numret bör höjas för att undvika dubbel kontroll nummer för de nummer som ännu inte har repliker ATS till det passiva området när katastrofen skedde i det aktiva området.</span><span class="sxs-lookup"><span data-stu-id="31779-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="31779-108">Ange om X12-eller EDIFACT kontroll nummer ska returneras med parametern "-AgreementType".</span><span class="sxs-lookup"><span data-stu-id="31779-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="31779-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="31779-109">EXAMPLES</span></span>

### <span data-ttu-id="31779-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="31779-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="31779-111">Det här kommandot får integrerings kontot som genererade X12 Interchange Control-nummer efter avtals namn.</span><span class="sxs-lookup"><span data-stu-id="31779-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="31779-112">Kontrol lera att angivet avtal är av typen "X12"</span><span class="sxs-lookup"><span data-stu-id="31779-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="31779-113">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="31779-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="31779-114">Det här kommandot får integrerings kontot som genererade EDIFACT Interchange Control-nummer efter avtals namn.</span><span class="sxs-lookup"><span data-stu-id="31779-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="31779-115">Kontrol lera att angivet avtal är av typen "EDIFACT"</span><span class="sxs-lookup"><span data-stu-id="31779-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="31779-116">Exempel 3</span><span class="sxs-lookup"><span data-stu-id="31779-116">Example 3</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1"
ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement1
IsMessageProcessingFailed:

ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement2
IsMessageProcessingFailed:

ControlNumber            : No generated control number was found for this agreement.
ControlNumberChangedTime : 1/1/0001 12:00:00 AM
AgreementName            : X12IntegrationAccountAgreement3
IsMessageProcessingFailed:
```

<span data-ttu-id="31779-117">Det här kommandot får alla genererade X12 Interchange Control-nummer efter integrations konto namn.</span><span class="sxs-lookup"><span data-stu-id="31779-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="31779-118">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="31779-118">PARAMETERS</span></span>

### <span data-ttu-id="31779-119">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="31779-119">-AgreementName</span></span>
<span data-ttu-id="31779-120">Namnet på integrerings konto avtalet.</span><span class="sxs-lookup"><span data-stu-id="31779-120">The integration account agreement name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31779-121">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="31779-121">-AgreementType</span></span>
<span data-ttu-id="31779-122">Avtals typen integrerings konto.</span><span class="sxs-lookup"><span data-stu-id="31779-122">The integration account agreement type.</span></span>

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

### <span data-ttu-id="31779-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31779-123">-DefaultProfile</span></span>
<span data-ttu-id="31779-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="31779-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31779-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="31779-125">-Name</span></span>
<span data-ttu-id="31779-126">Namn på integrations konto.</span><span class="sxs-lookup"><span data-stu-id="31779-126">The integration account name.</span></span>

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

### <span data-ttu-id="31779-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31779-127">-ResourceGroupName</span></span>
<span data-ttu-id="31779-128">Namnet på integrations konto resursen.</span><span class="sxs-lookup"><span data-stu-id="31779-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="31779-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31779-129">CommonParameters</span></span>
<span data-ttu-id="31779-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31779-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31779-131">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31779-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31779-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="31779-132">INPUTS</span></span>

### <span data-ttu-id="31779-133">System. String</span><span class="sxs-lookup"><span data-stu-id="31779-133">System.String</span></span>

## <span data-ttu-id="31779-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="31779-134">OUTPUTS</span></span>

### <span data-ttu-id="31779-135">Microsoft. Azure. commands. LogicApp. Utilities. IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="31779-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="31779-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="31779-136">NOTES</span></span>

## <span data-ttu-id="31779-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="31779-137">RELATED LINKS</span></span>

[<span data-ttu-id="31779-138">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="31779-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)

