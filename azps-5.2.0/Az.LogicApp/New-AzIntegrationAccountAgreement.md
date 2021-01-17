---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 190745ce8b09bf29b3cc3cbc07f35899732f97f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98388383"
---
# <span data-ttu-id="23e59-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="23e59-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="23e59-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="23e59-102">SYNOPSIS</span></span>
<span data-ttu-id="23e59-103">Skapar ett integrerings konto avtal.</span><span class="sxs-lookup"><span data-stu-id="23e59-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="23e59-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="23e59-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23e59-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="23e59-105">DESCRIPTION</span></span>
<span data-ttu-id="23e59-106">**New-AzIntegrationAccountAgreement-** cmdleten skapar ett integrerings konto avtal.</span><span class="sxs-lookup"><span data-stu-id="23e59-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="23e59-107">Denna cmdlet returnerar ett objekt som representerar integrerings konto avtalet.</span><span class="sxs-lookup"><span data-stu-id="23e59-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="23e59-108">Ange integrerings konto namn, resurs grupp namn, avtals namn, typ, partner namn, partner kvalificerare och avtals innehåll.</span><span class="sxs-lookup"><span data-stu-id="23e59-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="23e59-109">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="23e59-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="23e59-110">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="23e59-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="23e59-111">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="23e59-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="23e59-112">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="23e59-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="23e59-113">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="23e59-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="23e59-114">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="23e59-114">EXAMPLES</span></span>

### <span data-ttu-id="23e59-115">Exempel 1: skapa ett integrerings konto avtal</span><span class="sxs-lookup"><span data-stu-id="23e59-115">Example 1: Create a integration account agreement</span></span>
```powershell
PS C:\>New-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="23e59-116">Det här kommandot skapar ett integrerings konto avtal i den angivna Azure resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="23e59-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="23e59-117">Exempel 2</span><span class="sxs-lookup"><span data-stu-id="23e59-117">Example 2</span></span>

<span data-ttu-id="23e59-118">Skapar ett integrerings konto avtal.</span><span class="sxs-lookup"><span data-stu-id="23e59-118">Creates an integration account agreement.</span></span> <span data-ttu-id="23e59-119">(automatiskt genererat)</span><span class="sxs-lookup"><span data-stu-id="23e59-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountAgreement -AgreementContent <String> -AgreementName 'IntegrationAccountAgreement06' -AgreementType X12 -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="23e59-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="23e59-120">PARAMETERS</span></span>

### <span data-ttu-id="23e59-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="23e59-121">-AgreementContent</span></span>
<span data-ttu-id="23e59-122">Anger avtalets innehåll i JSON-format (Java Object Notation) för avtalet.</span><span class="sxs-lookup"><span data-stu-id="23e59-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="23e59-123">Ange antingen den här parametern eller parametern *AgreementContentFilePath* .</span><span class="sxs-lookup"><span data-stu-id="23e59-123">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="23e59-124">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="23e59-124">-AgreementContentFilePath</span></span>
<span data-ttu-id="23e59-125">Anger fil Sök vägen för avtalets innehåll.</span><span class="sxs-lookup"><span data-stu-id="23e59-125">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="23e59-126">Ange antingen den här parametern eller parametern *AgreementContent* .</span><span class="sxs-lookup"><span data-stu-id="23e59-126">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="23e59-127">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="23e59-127">-AgreementName</span></span>
<span data-ttu-id="23e59-128">Anger ett namn för integrerings konto avtalet.</span><span class="sxs-lookup"><span data-stu-id="23e59-128">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="23e59-129">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="23e59-129">-AgreementType</span></span>
<span data-ttu-id="23e59-130">Anger avtals typen för integrerings kontot.</span><span class="sxs-lookup"><span data-stu-id="23e59-130">Specifies the integration account agreement type.</span></span> <span data-ttu-id="23e59-131">De acceptabla värdena för den här parametern är:</span><span class="sxs-lookup"><span data-stu-id="23e59-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="23e59-132">X12</span><span class="sxs-lookup"><span data-stu-id="23e59-132">X12</span></span> 
- <span data-ttu-id="23e59-133">AS2</span><span class="sxs-lookup"><span data-stu-id="23e59-133">AS2</span></span>
- <span data-ttu-id="23e59-134">Edifact</span><span class="sxs-lookup"><span data-stu-id="23e59-134">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23e59-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23e59-135">-DefaultProfile</span></span>
<span data-ttu-id="23e59-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="23e59-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23e59-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="23e59-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="23e59-138">Anger en namn avgränsare för företags identitet för gäst partnern.</span><span class="sxs-lookup"><span data-stu-id="23e59-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="23e59-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="23e59-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="23e59-140">Integrations konto avtalets värde för gäst identitet.</span><span class="sxs-lookup"><span data-stu-id="23e59-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="23e59-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="23e59-141">-GuestPartner</span></span>
<span data-ttu-id="23e59-142">Anger namnet på gäst partnern.</span><span class="sxs-lookup"><span data-stu-id="23e59-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="23e59-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="23e59-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="23e59-144">Anger en namn avgränsare för företags identitet för värd partnern.</span><span class="sxs-lookup"><span data-stu-id="23e59-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="23e59-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="23e59-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="23e59-146">Integrerings värde för värden för värd identitet för integrations konto avtal.</span><span class="sxs-lookup"><span data-stu-id="23e59-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="23e59-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="23e59-147">-HostPartner</span></span>
<span data-ttu-id="23e59-148">Anger namnet på värd partnern.</span><span class="sxs-lookup"><span data-stu-id="23e59-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="23e59-149">-Metadata</span><span class="sxs-lookup"><span data-stu-id="23e59-149">-Metadata</span></span>
<span data-ttu-id="23e59-150">Anger ett metadataobjekt för avtalet.</span><span class="sxs-lookup"><span data-stu-id="23e59-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="23e59-151">-Namn</span><span class="sxs-lookup"><span data-stu-id="23e59-151">-Name</span></span>
<span data-ttu-id="23e59-152">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="23e59-152">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="23e59-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23e59-153">-ResourceGroupName</span></span>
<span data-ttu-id="23e59-154">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="23e59-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="23e59-155">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="23e59-155">-Confirm</span></span>
<span data-ttu-id="23e59-156">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="23e59-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23e59-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23e59-157">-WhatIf</span></span>
<span data-ttu-id="23e59-158">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="23e59-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23e59-159">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="23e59-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23e59-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e59-160">CommonParameters</span></span>
<span data-ttu-id="23e59-161">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23e59-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e59-162">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23e59-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e59-163">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="23e59-163">INPUTS</span></span>

### <span data-ttu-id="23e59-164">System. String</span><span class="sxs-lookup"><span data-stu-id="23e59-164">System.String</span></span>

## <span data-ttu-id="23e59-165">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="23e59-165">OUTPUTS</span></span>

### <span data-ttu-id="23e59-166">Microsoft. Azure. Management. Logic. Models. IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="23e59-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="23e59-167">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="23e59-167">NOTES</span></span>

## <span data-ttu-id="23e59-168">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="23e59-168">RELATED LINKS</span></span>

[<span data-ttu-id="23e59-169">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="23e59-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="23e59-170">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="23e59-170">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="23e59-171">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="23e59-171">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


