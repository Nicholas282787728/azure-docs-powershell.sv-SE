---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 651ce1141e9a925d5571f8b70d8eecedb4a1e66d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089599"
---
# <span data-ttu-id="5d56f-101">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="5d56f-101">New-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="5d56f-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="5d56f-102">SYNOPSIS</span></span>
<span data-ttu-id="5d56f-103">Skapar ett integrerings konto certifikat.</span><span class="sxs-lookup"><span data-stu-id="5d56f-103">Creates an integration account certificate.</span></span>

## <span data-ttu-id="5d56f-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="5d56f-104">SYNTAX</span></span>

### <span data-ttu-id="5d56f-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="5d56f-105">PrivateKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d56f-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="5d56f-106">PublicKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d56f-107">Varken</span><span class="sxs-lookup"><span data-stu-id="5d56f-107">Both</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d56f-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="5d56f-108">DESCRIPTION</span></span>
<span data-ttu-id="5d56f-109">Cmdleten **New-AzIntegrationAccountCertificate** skapar ett integrerings konto certifikat.</span><span class="sxs-lookup"><span data-stu-id="5d56f-109">The **New-AzIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="5d56f-110">Denna cmdlet returnerar ett objekt som representerar integrerings konto certifikatet.</span><span class="sxs-lookup"><span data-stu-id="5d56f-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="5d56f-111">Ange integrerings konto namn, resurs grupps namn, certifikat namn, namn på nycklar och ID för valv.</span><span class="sxs-lookup"><span data-stu-id="5d56f-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="5d56f-112">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="5d56f-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="5d56f-113">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="5d56f-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5d56f-114">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="5d56f-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5d56f-115">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="5d56f-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5d56f-116">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="5d56f-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5d56f-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="5d56f-117">EXAMPLES</span></span>

### <span data-ttu-id="5d56f-118">Exempel 1: skapa ett integrerings konto certifikat</span><span class="sxs-lookup"><span data-stu-id="5d56f-118">Example 1: Create an integration account certificate</span></span>
```
PS C:\>New-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="5d56f-119">Det här kommandot skapar integrerings konto certifikatet i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="5d56f-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="5d56f-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="5d56f-120">PARAMETERS</span></span>

### <span data-ttu-id="5d56f-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="5d56f-121">-CertificateName</span></span>
<span data-ttu-id="5d56f-122">Anger ett namn på integrations konto certifikatet.</span><span class="sxs-lookup"><span data-stu-id="5d56f-122">Specifies a name for the integration account certificate.</span></span>

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

### <span data-ttu-id="5d56f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d56f-123">-DefaultProfile</span></span>
<span data-ttu-id="5d56f-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="5d56f-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d56f-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="5d56f-125">-KeyName</span></span>
<span data-ttu-id="5d56f-126">Anger namnet på certifikats nycklar i nyckelords valvet.</span><span class="sxs-lookup"><span data-stu-id="5d56f-126">Specifies the name of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d56f-127">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="5d56f-127">-KeyVaultId</span></span>
<span data-ttu-id="5d56f-128">Anger ett valv-ID.</span><span class="sxs-lookup"><span data-stu-id="5d56f-128">Specifies a key vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d56f-129">-Version</span><span class="sxs-lookup"><span data-stu-id="5d56f-129">-KeyVersion</span></span>
<span data-ttu-id="5d56f-130">Anger vilken version av certifikats nycklar som visas i nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="5d56f-130">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d56f-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="5d56f-131">-Metadata</span></span>
<span data-ttu-id="5d56f-132">Anger ett metadataobjekt för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="5d56f-132">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="5d56f-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="5d56f-133">-Name</span></span>
<span data-ttu-id="5d56f-134">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="5d56f-134">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="5d56f-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="5d56f-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="5d56f-136">Anger sökvägen till ett offentlig certifikat (CER-fil).</span><span class="sxs-lookup"><span data-stu-id="5d56f-136">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d56f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d56f-137">-ResourceGroupName</span></span>
<span data-ttu-id="5d56f-138">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="5d56f-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5d56f-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="5d56f-139">-Confirm</span></span>
<span data-ttu-id="5d56f-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="5d56f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d56f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d56f-141">-WhatIf</span></span>
<span data-ttu-id="5d56f-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="5d56f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d56f-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="5d56f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d56f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d56f-144">CommonParameters</span></span>
<span data-ttu-id="5d56f-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d56f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d56f-146">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d56f-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d56f-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="5d56f-147">INPUTS</span></span>

### <span data-ttu-id="5d56f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="5d56f-148">System.String</span></span>

## <span data-ttu-id="5d56f-149">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="5d56f-149">OUTPUTS</span></span>

### <span data-ttu-id="5d56f-150">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="5d56f-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="5d56f-151">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="5d56f-151">NOTES</span></span>

## <span data-ttu-id="5d56f-152">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="5d56f-152">RELATED LINKS</span></span>

[<span data-ttu-id="5d56f-153">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="5d56f-153">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="5d56f-154">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="5d56f-154">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="5d56f-155">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="5d56f-155">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


