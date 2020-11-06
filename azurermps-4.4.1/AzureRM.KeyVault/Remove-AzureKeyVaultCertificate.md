---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
ms.openlocfilehash: 9a33d4efdd82ad03b94ea9a7e862fb5e13eb30d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93585500"
---
# <span data-ttu-id="c703a-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c703a-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="c703a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c703a-102">SYNOPSIS</span></span>
<span data-ttu-id="c703a-103">Tar bort ett certifikat från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="c703a-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c703a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c703a-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c703a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c703a-105">DESCRIPTION</span></span>
<span data-ttu-id="c703a-106">Cmdleten **Remove-AzureKeyVaultCertificate** tar bort ett certifikat från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="c703a-106">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="c703a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c703a-107">EXAMPLES</span></span>

### <span data-ttu-id="c703a-108">Exempel 1: ta bort ett certifikat</span><span class="sxs-lookup"><span data-stu-id="c703a-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="c703a-109">Det här kommandot tar bort certifikatet som heter SelfSigned01 från Key-valvet med namnet ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="c703a-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="c703a-110">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="c703a-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c703a-111">Därför behöver du inte bekräfta en bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c703a-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="c703a-112">Exempel 3: ta bort det borttagna certifikatet från Key Vault permanent</span><span class="sxs-lookup"><span data-stu-id="c703a-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="c703a-113">Det här kommandot tar permanent bort certifikatet med namnet ' mitt certifikat ' från huvud valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="c703a-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="c703a-114">För att köra denna cmdlet krävs "Rensa"-behörigheten, som måste dessförinnan och uttryckligen ges till användaren i det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="c703a-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="c703a-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c703a-115">PARAMETERS</span></span>

### <span data-ttu-id="c703a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c703a-116">-Force</span></span>
<span data-ttu-id="c703a-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c703a-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c703a-118">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="c703a-118">-InRemovedState</span></span>
<span data-ttu-id="c703a-119">Om den visas tar du bort det borttagna certifikatet permanent.</span><span class="sxs-lookup"><span data-stu-id="c703a-119">If present, removes the previously deleted certificate permanently.</span></span>

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

### <span data-ttu-id="c703a-120">-Namn</span><span class="sxs-lookup"><span data-stu-id="c703a-120">-Name</span></span>
<span data-ttu-id="c703a-121">Anger namnet på det certifikat som denna cmdlet tar bort från ett valv.</span><span class="sxs-lookup"><span data-stu-id="c703a-121">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="c703a-122">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för ett certifikat baserat på namnet som den här parametern anger, namnet på Key-valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="c703a-122">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c703a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c703a-123">-PassThru</span></span>
<span data-ttu-id="c703a-124">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="c703a-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c703a-125">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="c703a-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c703a-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c703a-126">-VaultName</span></span>
<span data-ttu-id="c703a-127">Anger namnet på det huvud valv som denna cmdlet tar bort ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="c703a-127">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="c703a-128">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="c703a-128">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c703a-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c703a-129">-Confirm</span></span>
<span data-ttu-id="c703a-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c703a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c703a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c703a-131">-WhatIf</span></span>
<span data-ttu-id="c703a-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c703a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c703a-133">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c703a-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c703a-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c703a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c703a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c703a-135">-DefaultProfile</span></span>
<span data-ttu-id="c703a-136">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="c703a-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c703a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c703a-137">CommonParameters</span></span>
<span data-ttu-id="c703a-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c703a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c703a-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c703a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c703a-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c703a-140">INPUTS</span></span>

## <span data-ttu-id="c703a-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c703a-141">OUTPUTS</span></span>

### <span data-ttu-id="c703a-142">Microsoft. Azure. commands. valv. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="c703a-142">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="c703a-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c703a-143">NOTES</span></span>

## <span data-ttu-id="c703a-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c703a-144">RELATED LINKS</span></span>

[<span data-ttu-id="c703a-145">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c703a-145">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="c703a-146">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c703a-146">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="c703a-147">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c703a-147">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="c703a-148">Ångra-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="c703a-148">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
