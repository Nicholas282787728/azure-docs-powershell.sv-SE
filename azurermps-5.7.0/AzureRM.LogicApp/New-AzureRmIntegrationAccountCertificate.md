---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 555da1343813884a1f773d199cb99a188f7efedc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93580411"
---
# <span data-ttu-id="971d9-101">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="971d9-101">New-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="971d9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="971d9-102">SYNOPSIS</span></span>
<span data-ttu-id="971d9-103">Skapar ett integrerings konto certifikat.</span><span class="sxs-lookup"><span data-stu-id="971d9-103">Creates an integration account certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="971d9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="971d9-104">SYNTAX</span></span>

### <span data-ttu-id="971d9-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="971d9-105">PrivateKey</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="971d9-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="971d9-106">PublicKey</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="971d9-107">Varken</span><span class="sxs-lookup"><span data-stu-id="971d9-107">Both</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="971d9-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="971d9-108">DESCRIPTION</span></span>
<span data-ttu-id="971d9-109">Cmdleten **New-AzureRmIntegrationAccountCertificate** skapar ett integrerings konto certifikat.</span><span class="sxs-lookup"><span data-stu-id="971d9-109">The **New-AzureRmIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="971d9-110">Denna cmdlet returnerar ett objekt som representerar integrerings konto certifikatet.</span><span class="sxs-lookup"><span data-stu-id="971d9-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="971d9-111">Ange integrerings konto namn, resurs grupps namn, certifikat namn, namn på nycklar och ID för valv.</span><span class="sxs-lookup"><span data-stu-id="971d9-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="971d9-112">De fil värden för mallfiler som du anger i kommando raden har högre prioritet än värden för Mallkategorier i ett Template parameter-objekt.</span><span class="sxs-lookup"><span data-stu-id="971d9-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="971d9-113">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="971d9-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="971d9-114">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="971d9-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="971d9-115">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="971d9-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="971d9-116">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="971d9-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="971d9-117">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="971d9-117">EXAMPLES</span></span>

### <span data-ttu-id="971d9-118">Exempel 1: skapa ett integrerings konto certifikat</span><span class="sxs-lookup"><span data-stu-id="971d9-118">Example 1: Create an integration account certificate</span></span>
```
PS C:\>New-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="971d9-119">Det här kommandot skapar integrerings konto certifikatet i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="971d9-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="971d9-120">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="971d9-120">PARAMETERS</span></span>

### <span data-ttu-id="971d9-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="971d9-121">-CertificateName</span></span>
<span data-ttu-id="971d9-122">Anger ett namn på integrations konto certifikatet.</span><span class="sxs-lookup"><span data-stu-id="971d9-122">Specifies a name for the integration account certificate.</span></span>

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

### <span data-ttu-id="971d9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="971d9-123">-DefaultProfile</span></span>
<span data-ttu-id="971d9-124">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="971d9-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="971d9-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="971d9-125">-KeyName</span></span>
<span data-ttu-id="971d9-126">Anger namnet på certifikats nycklar i nyckelords valvet.</span><span class="sxs-lookup"><span data-stu-id="971d9-126">Specifies the name of the certificate key in the key vault.</span></span>

```yaml
Type: String
Parameter Sets: PrivateKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: PublicKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="971d9-127">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="971d9-127">-KeyVaultId</span></span>
<span data-ttu-id="971d9-128">Anger ett valv-ID.</span><span class="sxs-lookup"><span data-stu-id="971d9-128">Specifies a key vault ID.</span></span>

```yaml
Type: String
Parameter Sets: PrivateKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: PublicKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="971d9-129">-Version</span><span class="sxs-lookup"><span data-stu-id="971d9-129">-KeyVersion</span></span>
<span data-ttu-id="971d9-130">Anger vilken version av certifikats nycklar som visas i nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="971d9-130">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: String
Parameter Sets: PrivateKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: PublicKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="971d9-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="971d9-131">-Metadata</span></span>
<span data-ttu-id="971d9-132">Anger ett metadataobjekt för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="971d9-132">Specifies a metadata object for the certificate.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="971d9-133">-Namn</span><span class="sxs-lookup"><span data-stu-id="971d9-133">-Name</span></span>
<span data-ttu-id="971d9-134">Anger namnet på ett integrations konto.</span><span class="sxs-lookup"><span data-stu-id="971d9-134">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="971d9-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="971d9-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="971d9-136">Anger sökvägen till ett offentlig certifikat (CER-fil).</span><span class="sxs-lookup"><span data-stu-id="971d9-136">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: String
Parameter Sets: PrivateKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: PublicKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="971d9-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="971d9-137">-ResourceGroupName</span></span>
<span data-ttu-id="971d9-138">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="971d9-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="971d9-139">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="971d9-139">-Confirm</span></span>
<span data-ttu-id="971d9-140">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="971d9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="971d9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="971d9-141">-WhatIf</span></span>
<span data-ttu-id="971d9-142">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="971d9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="971d9-143">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="971d9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="971d9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="971d9-144">CommonParameters</span></span>
<span data-ttu-id="971d9-145">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="971d9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="971d9-146">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="971d9-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="971d9-147">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="971d9-147">INPUTS</span></span>

### <span data-ttu-id="971d9-148">Ingen</span><span class="sxs-lookup"><span data-stu-id="971d9-148">None</span></span>
<span data-ttu-id="971d9-149">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="971d9-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="971d9-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="971d9-150">OUTPUTS</span></span>

### <span data-ttu-id="971d9-151">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="971d9-151">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="971d9-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="971d9-152">NOTES</span></span>

## <span data-ttu-id="971d9-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="971d9-153">RELATED LINKS</span></span>

[<span data-ttu-id="971d9-154">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="971d9-154">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="971d9-155">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="971d9-155">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="971d9-156">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="971d9-156">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


