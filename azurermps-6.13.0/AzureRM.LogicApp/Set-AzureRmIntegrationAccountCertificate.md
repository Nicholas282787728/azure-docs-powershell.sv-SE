---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 00acd3e13484fe2981d172b4331ff7848c78fc9a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582648"
---
# <span data-ttu-id="6714b-101">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="6714b-101">Set-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="6714b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="6714b-102">SYNOPSIS</span></span>
<span data-ttu-id="6714b-103">Ändrar ett integrerings konto certifikat.</span><span class="sxs-lookup"><span data-stu-id="6714b-103">Modifies an integration account certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6714b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="6714b-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6714b-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="6714b-105">DESCRIPTION</span></span>
<span data-ttu-id="6714b-106">Cmdleten **set-AzureRmIntegrationAccountCertificate** ändrar ett integrerings konto certifikat.</span><span class="sxs-lookup"><span data-stu-id="6714b-106">The **Set-AzureRmIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="6714b-107">Denna cmdlet returnerar ett objekt som representerar integrerings konto certifikatet.</span><span class="sxs-lookup"><span data-stu-id="6714b-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="6714b-108">Ange integrerings konto namn, resurs grupps namn och certifikat namn.</span><span class="sxs-lookup"><span data-stu-id="6714b-108">Specifying the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="6714b-109">Den här modulen stöder dynamiska parametrar.</span><span class="sxs-lookup"><span data-stu-id="6714b-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6714b-110">Om du vill använda en dynamisk parameter skriver du den i kommandot.</span><span class="sxs-lookup"><span data-stu-id="6714b-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6714b-111">Om du vill söka efter namn på dynamiska parametrar skriver du ett bindestreck (-) efter cmdlet-namnet och trycker sedan på TABB-tangenten flera gånger för att växla mellan de tillgängliga parametrarna.</span><span class="sxs-lookup"><span data-stu-id="6714b-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6714b-112">Om du utelämnar en obligatorisk mallparameter frågar cmdleten efter värdet.</span><span class="sxs-lookup"><span data-stu-id="6714b-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6714b-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="6714b-113">EXAMPLES</span></span>

### <span data-ttu-id="6714b-114">Exempel 1: ändra ett integrations konto certifikat</span><span class="sxs-lookup"><span data-stu-id="6714b-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegartionAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="6714b-115">Det här kommandot ändrar det integrerade konto certifikatet i den angivna resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="6714b-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="6714b-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="6714b-116">PARAMETERS</span></span>

### <span data-ttu-id="6714b-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="6714b-117">-CertificateName</span></span>
<span data-ttu-id="6714b-118">Anger namnet på ett integrations konto certifikat.</span><span class="sxs-lookup"><span data-stu-id="6714b-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="6714b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6714b-119">-DefaultProfile</span></span>
<span data-ttu-id="6714b-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="6714b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6714b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6714b-121">-Force</span></span>
<span data-ttu-id="6714b-122">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="6714b-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6714b-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="6714b-123">-KeyName</span></span>
<span data-ttu-id="6714b-124">Anger namnet på en certifikats nycklar i nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="6714b-124">Specifies the name of a certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6714b-125">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="6714b-125">-KeyVaultId</span></span>
<span data-ttu-id="6714b-126">Anger ett valv-ID.</span><span class="sxs-lookup"><span data-stu-id="6714b-126">Specifies a key vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6714b-127">-Version</span><span class="sxs-lookup"><span data-stu-id="6714b-127">-KeyVersion</span></span>
<span data-ttu-id="6714b-128">Anger vilken version av certifikats nycklar som visas i nyckelordet.</span><span class="sxs-lookup"><span data-stu-id="6714b-128">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6714b-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="6714b-129">-Metadata</span></span>
<span data-ttu-id="6714b-130">Anger ett metadataobjekt för certifikatet.</span><span class="sxs-lookup"><span data-stu-id="6714b-130">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="6714b-131">-Namn</span><span class="sxs-lookup"><span data-stu-id="6714b-131">-Name</span></span>
<span data-ttu-id="6714b-132">Anger namnet på integrations kontot.</span><span class="sxs-lookup"><span data-stu-id="6714b-132">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="6714b-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="6714b-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="6714b-134">Anger sökvägen till ett offentlig certifikat (CER-fil).</span><span class="sxs-lookup"><span data-stu-id="6714b-134">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6714b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6714b-135">-ResourceGroupName</span></span>
<span data-ttu-id="6714b-136">Anger namnet på en resurs grupp.</span><span class="sxs-lookup"><span data-stu-id="6714b-136">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6714b-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="6714b-137">-Confirm</span></span>
<span data-ttu-id="6714b-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="6714b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6714b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6714b-139">-WhatIf</span></span>
<span data-ttu-id="6714b-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="6714b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6714b-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="6714b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6714b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6714b-142">CommonParameters</span></span>
<span data-ttu-id="6714b-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6714b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6714b-144">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6714b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6714b-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="6714b-145">INPUTS</span></span>

### <span data-ttu-id="6714b-146">System. String</span><span class="sxs-lookup"><span data-stu-id="6714b-146">System.String</span></span>

## <span data-ttu-id="6714b-147">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="6714b-147">OUTPUTS</span></span>

### <span data-ttu-id="6714b-148">Microsoft. Azure. Management. Logic. Models. IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="6714b-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="6714b-149">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="6714b-149">NOTES</span></span>

## <span data-ttu-id="6714b-150">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="6714b-150">RELATED LINKS</span></span>

[<span data-ttu-id="6714b-151">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="6714b-151">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="6714b-152">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="6714b-152">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="6714b-153">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="6714b-153">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

