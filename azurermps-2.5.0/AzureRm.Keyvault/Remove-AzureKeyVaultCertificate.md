---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: 662304cff991da0d9ffe9d946e63bc94ba51e4a9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928821"
---
# <span data-ttu-id="dbece-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="dbece-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="dbece-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="dbece-102">SYNOPSIS</span></span>
<span data-ttu-id="dbece-103">Tar bort ett certifikat från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="dbece-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbece-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="dbece-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbece-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="dbece-105">DESCRIPTION</span></span>
<span data-ttu-id="dbece-106">Cmdleten **Remove-AzureKeyVaultCertificate** tar bort ett certifikat från ett nyckelord.</span><span class="sxs-lookup"><span data-stu-id="dbece-106">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="dbece-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="dbece-107">EXAMPLES</span></span>

### <span data-ttu-id="dbece-108">Exempel 1: ta bort ett certifikat</span><span class="sxs-lookup"><span data-stu-id="dbece-108">Example 1: Remove a certificate</span></span>
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

<span data-ttu-id="dbece-109">Det här kommandot tar bort certifikatet som heter SelfSigned01 från Key-valvet med namnet ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="dbece-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="dbece-110">Det här kommandot anger parametern *Force* .</span><span class="sxs-lookup"><span data-stu-id="dbece-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="dbece-111">Därför behöver du inte bekräfta en bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="dbece-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="dbece-112">Exempel 3: ta bort det borttagna certifikatet från Key Vault permanent</span><span class="sxs-lookup"><span data-stu-id="dbece-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="dbece-113">Det här kommandot tar permanent bort certifikatet med namnet ' mitt certifikat ' från huvud valvet med namnet contoso.</span><span class="sxs-lookup"><span data-stu-id="dbece-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="dbece-114">För att köra denna cmdlet krävs "Rensa"-behörigheten, som måste dessförinnan och uttryckligen ges till användaren i det här nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="dbece-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="dbece-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="dbece-115">PARAMETERS</span></span>

### <span data-ttu-id="dbece-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbece-116">-DefaultProfile</span></span>
<span data-ttu-id="dbece-117">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="dbece-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dbece-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dbece-118">-Force</span></span>
<span data-ttu-id="dbece-119">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="dbece-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbece-120">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="dbece-120">-InRemovedState</span></span>
<span data-ttu-id="dbece-121">Om det finns någon tar bort det tidigare borttagna certifikatet permanent</span><span class="sxs-lookup"><span data-stu-id="dbece-121">If present, removes the previously deleted certificate permanently</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbece-122">-Namn</span><span class="sxs-lookup"><span data-stu-id="dbece-122">-Name</span></span>
<span data-ttu-id="dbece-123">Anger namnet på det certifikat som denna cmdlet tar bort från ett valv.</span><span class="sxs-lookup"><span data-stu-id="dbece-123">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="dbece-124">Denna cmdlet konstruerar det fullständigt kvalificerade domän namnet (FQDN) för ett certifikat baserat på namnet som den här parametern anger, namnet på Key-valvet och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="dbece-124">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbece-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbece-125">-PassThru</span></span>
<span data-ttu-id="dbece-126">Returnerar ett objekt som representerar det objekt som du arbetar med.</span><span class="sxs-lookup"><span data-stu-id="dbece-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dbece-127">Denna cmdlet genererar som standard inga utdata.</span><span class="sxs-lookup"><span data-stu-id="dbece-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbece-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="dbece-128">-VaultName</span></span>
<span data-ttu-id="dbece-129">Anger namnet på det huvud valv som denna cmdlet tar bort ett certifikat för.</span><span class="sxs-lookup"><span data-stu-id="dbece-129">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="dbece-130">Denna cmdlet konstruerar FQDN för ett Key valv baserat på namnet som den här parametern anger och din nuvarande miljö.</span><span class="sxs-lookup"><span data-stu-id="dbece-130">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dbece-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="dbece-131">-Confirm</span></span>
<span data-ttu-id="dbece-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="dbece-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbece-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbece-133">-WhatIf</span></span>
<span data-ttu-id="dbece-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dbece-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbece-135">Cmdleten körs inte. Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="dbece-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbece-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="dbece-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbece-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbece-137">CommonParameters</span></span>
<span data-ttu-id="dbece-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbece-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbece-139">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbece-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbece-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="dbece-140">INPUTS</span></span>

## <span data-ttu-id="dbece-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="dbece-141">OUTPUTS</span></span>

### <span data-ttu-id="dbece-142">Microsoft. Azure. commands. valv. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="dbece-142">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="dbece-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="dbece-143">NOTES</span></span>

## <span data-ttu-id="dbece-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="dbece-144">RELATED LINKS</span></span>

[<span data-ttu-id="dbece-145">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="dbece-145">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="dbece-146">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="dbece-146">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="dbece-147">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="dbece-147">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="dbece-148">Ångra-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="dbece-148">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
