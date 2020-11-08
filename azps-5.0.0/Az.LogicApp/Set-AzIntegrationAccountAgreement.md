---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
ms.openlocfilehash: ac0e5e89706e648d714e3f09ebad5dee7d7b4416
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94272183"
---
# <span data-ttu-id="d8fc0-101">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d8fc0-101">Set-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="d8fc0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="d8fc0-102">SYNOPSIS</span></span>
<span data-ttu-id="d8fc0-103">Ändrar ett integrerings konto avtal.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-103">Modifies an integration account agreement.</span></span>

## <span data-ttu-id="d8fc0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="d8fc0-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8fc0-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="d8fc0-105">DESCRIPTION</span></span>
<span data-ttu-id="d8fc0-106">Cmdleten **set-AzIntegrationAccountAgreement** ändrar ett integrerings konto avtal.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-106">The **Set-AzIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="d8fc0-107">Denna cmdlet returnerar ett objekt som representerar integrerings konto avtalet.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="d8fc0-108">Ange integrerings konto namn, resurs grupps namn och avtals namn.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-108">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="d8fc0-109">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="d8fc0-110">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d8fc0-111">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d8fc0-112">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d8fc0-113">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d8fc0-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="d8fc0-114">EXAMPLES</span></span>

### <span data-ttu-id="d8fc0-115">Exempel 1: uppdatera ett integrerings konto avtal</span><span class="sxs-lookup"><span data-stu-id="d8fc0-115">Example 1: Update an integration account agreement</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/agreements/IntegrationAccountAgreement06
Name                   : IntegrationAccountAgreement06
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/26/2016 6:43:52 PM
ChangedTime            : 3/26/2016 6:43:52 PM
AgreementType          : X12
HostPartner            : HostPartner
GuestPartner           : GuestPartner
HostIdentityQualifier  : AA
HostIdentityValue      : AA
GuestIdentityQualifier : BB
GuestIdentityValue     : BB
Content                : {"AS2":null,"X12":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ","Valu
                         e":"ZZ"},"ProtocolSettings":{"ValidationSettings":{"ValidateCharacterSet":true,"CheckDuplicateInterchangeControlNumber":false,"InterchangeControlN
                         . . .
```

<span data-ttu-id="d8fc0-116">Det här kommandot uppdaterar ett integrerings konto avtal i den angivna Azure resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="d8fc0-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="d8fc0-117">Example 2</span></span>

<span data-ttu-id="d8fc0-118">Ändrar ett integrerings konto avtal.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-118">Modifies an integration account agreement.</span></span> <span data-ttu-id="d8fc0-119">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="d8fc0-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountAgreement -AgreementContentFilePath 'C:\temp\AgreementContent.json' -AgreementName 'IntegrationAccountAgreement06' -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Metadata <Object> -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="d8fc0-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="d8fc0-120">PARAMETERS</span></span>

### <span data-ttu-id="d8fc0-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="d8fc0-121">-AgreementContent</span></span>
<span data-ttu-id="d8fc0-122">Anger avtalets innehåll i JSON-format (Java Object Notation) för avtalet.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="d8fc0-123">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="d8fc0-123">-AgreementContentFilePath</span></span>
<span data-ttu-id="d8fc0-124">Anger fil Sök vägen för avtalets innehåll.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-124">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="d8fc0-125">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="d8fc0-125">-AgreementName</span></span>
<span data-ttu-id="d8fc0-126">Anger namnet på integrerings konto avtalet.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-126">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="d8fc0-127">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="d8fc0-127">-AgreementType</span></span>
<span data-ttu-id="d8fc0-128">Anger avtals typen för integrerings kontot.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-128">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="d8fc0-129">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="d8fc0-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d8fc0-130">X12</span><span class="sxs-lookup"><span data-stu-id="d8fc0-130">X12</span></span> 
- <span data-ttu-id="d8fc0-131">AS2</span><span class="sxs-lookup"><span data-stu-id="d8fc0-131">AS2</span></span>
- <span data-ttu-id="d8fc0-132">Edifact</span><span class="sxs-lookup"><span data-stu-id="d8fc0-132">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8fc0-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8fc0-133">-DefaultProfile</span></span>
<span data-ttu-id="d8fc0-134">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="d8fc0-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8fc0-135">-Force</span><span class="sxs-lookup"><span data-stu-id="d8fc0-135">-Force</span></span>
<span data-ttu-id="d8fc0-136">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d8fc0-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="d8fc0-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="d8fc0-138">Anger en namn avgränsare för företags identitet för gäst partnern.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="d8fc0-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="d8fc0-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="d8fc0-140">Integrations konto avtalets värde för gäst identitet.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="d8fc0-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="d8fc0-141">-GuestPartner</span></span>
<span data-ttu-id="d8fc0-142">Anger namnet på gäst partnern.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="d8fc0-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="d8fc0-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="d8fc0-144">Anger en namn avgränsare för företags identitet för värd partnern.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="d8fc0-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="d8fc0-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="d8fc0-146">Integrerings värde för värden för värd identitet för integrations konto avtal.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="d8fc0-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="d8fc0-147">-HostPartner</span></span>
<span data-ttu-id="d8fc0-148">Anger namnet på värd partnern.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="d8fc0-149">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d8fc0-149">-Metadata</span></span>
<span data-ttu-id="d8fc0-150">Anger ett metadataobjekt för avtalet.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-150">Specifies a metadata object for the agreement.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8fc0-151">-Namn</span><span class="sxs-lookup"><span data-stu-id="d8fc0-151">-Name</span></span>
<span data-ttu-id="d8fc0-152">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-152">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="d8fc0-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8fc0-153">-ResourceGroupName</span></span>
<span data-ttu-id="d8fc0-154">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d8fc0-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="d8fc0-155">-Confirm</span></span>
<span data-ttu-id="d8fc0-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8fc0-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8fc0-157">-WhatIf</span></span>
<span data-ttu-id="d8fc0-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8fc0-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8fc0-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8fc0-160">CommonParameters</span></span>
<span data-ttu-id="d8fc0-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8fc0-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8fc0-162">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8fc0-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8fc0-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="d8fc0-163">INPUTS</span></span>

### <span data-ttu-id="d8fc0-164">System. String</span><span class="sxs-lookup"><span data-stu-id="d8fc0-164">System.String</span></span>

## <span data-ttu-id="d8fc0-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="d8fc0-165">OUTPUTS</span></span>

### <span data-ttu-id="d8fc0-166">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d8fc0-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="d8fc0-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="d8fc0-167">NOTES</span></span>

## <span data-ttu-id="d8fc0-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="d8fc0-168">RELATED LINKS</span></span>

[<span data-ttu-id="d8fc0-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d8fc0-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="d8fc0-170">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d8fc0-170">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="d8fc0-171">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="d8fc0-171">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)


