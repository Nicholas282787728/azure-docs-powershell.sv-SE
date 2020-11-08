---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
ms.openlocfilehash: 38e0dbf124643a7d669c1787314790166e88f6a9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94273431"
---
# <span data-ttu-id="7a0f6-101">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="7a0f6-101">Restore-AzManagedHsmKey</span></span>

## <span data-ttu-id="7a0f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7a0f6-102">SYNOPSIS</span></span>
<span data-ttu-id="7a0f6-103">Skapar en nycklar i en hanterad HSM från en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="7a0f6-103">Creates a key in a managed HSM from a backed-up key.</span></span>

## <span data-ttu-id="7a0f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7a0f6-104">SYNTAX</span></span>

### <span data-ttu-id="7a0f6-105">ByHsmName (standard)</span><span class="sxs-lookup"><span data-stu-id="7a0f6-105">ByHsmName (Default)</span></span>
```
Restore-AzManagedHsmKey [-HsmName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a0f6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7a0f6-106">ByInputObject</span></span>
```
Restore-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a0f6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7a0f6-107">ByResourceId</span></span>
```
Restore-AzManagedHsmKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a0f6-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7a0f6-108">DESCRIPTION</span></span>
<span data-ttu-id="7a0f6-109">Cmdleten **restore-AzManagedHsmKey** skapar en Key i den angivna hanterade HSM.</span><span class="sxs-lookup"><span data-stu-id="7a0f6-109">The **Restore-AzManagedHsmKey** cmdlet creates a key in the specified managed HSM.</span></span>
<span data-ttu-id="7a0f6-110">Den här tangenten är en replik av säkerhets kopian i indatafilen och har samma namn som den ursprungliga tangenten.</span><span class="sxs-lookup"><span data-stu-id="7a0f6-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="7a0f6-111">Om den hanterade HSM redan har en nycklar med samma namn, Miss lyckas denna cmdlet i stället för att skriva över den ursprungliga tangenten.</span><span class="sxs-lookup"><span data-stu-id="7a0f6-111">If the managed HSM already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="7a0f6-112">Om säkerhets kopian innehåller flera versioner av en, återställs alla versioner.</span><span class="sxs-lookup"><span data-stu-id="7a0f6-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="7a0f6-113">Den hanterade HSM som du återställer tangenten till kan skilja sig från den hanterade HSM som du säkerhetskopierade från.</span><span class="sxs-lookup"><span data-stu-id="7a0f6-113">The managed HSM that you restore the key into can be different from the managed HSM that you backed up the key from.</span></span>
<span data-ttu-id="7a0f6-114">Däremot måste hanterad HSM använda samma abonnemang och vara i ett Azure-område på samma geografi (till exempel Nord Amerika).</span><span class="sxs-lookup"><span data-stu-id="7a0f6-114">However, the managed HSM must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="7a0f6-115">Se Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) för kart läggning av Azure-regioner till olika länder.</span><span class="sxs-lookup"><span data-stu-id="7a0f6-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="7a0f6-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7a0f6-116">EXAMPLES</span></span>

### <span data-ttu-id="7a0f6-117">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="7a0f6-117">Example 1</span></span>
```powershell
PS C:\> Restore-AzManagedHsmKey -HsmName testmhsm -InputFile "C:\Backup.blob"

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 7cff8510da04433b98144a3e33ad2bae
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/7cff8510da04433b98144a3e33ad2bae
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 10:13:03 AM
Updated        : 10/14/2020 10:13:03 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="7a0f6-118">Det här kommandot återställer en-och alla dess versioner från säkerhets kopian med namnet Backup. blob till den hanterade HSM som heter testmhsm.</span><span class="sxs-lookup"><span data-stu-id="7a0f6-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the managed HSM named testmhsm.</span></span>

## <span data-ttu-id="7a0f6-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7a0f6-119">PARAMETERS</span></span>

### <span data-ttu-id="7a0f6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a0f6-120">-DefaultProfile</span></span>
<span data-ttu-id="7a0f6-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="7a0f6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a0f6-122">-HsmName</span><span class="sxs-lookup"><span data-stu-id="7a0f6-122">-HsmName</span></span>
<span data-ttu-id="7a0f6-123">HSM-namn.</span><span class="sxs-lookup"><span data-stu-id="7a0f6-123">HSM name.</span></span> <span data-ttu-id="7a0f6-124">Cmdlet konstruerar FQDN för en hanterad HSM baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="7a0f6-124">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHsmName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a0f6-125">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7a0f6-125">-InputFile</span></span>
<span data-ttu-id="7a0f6-126">Indatafil.</span><span class="sxs-lookup"><span data-stu-id="7a0f6-126">Input file.</span></span>
<span data-ttu-id="7a0f6-127">Den indatafil som innehåller den säkerhetskopierade blobben</span><span class="sxs-lookup"><span data-stu-id="7a0f6-127">The input file containing the backed-up blob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a0f6-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a0f6-128">-InputObject</span></span>
<span data-ttu-id="7a0f6-129">HSM-objekt</span><span class="sxs-lookup"><span data-stu-id="7a0f6-129">HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a0f6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a0f6-130">-ResourceId</span></span>
<span data-ttu-id="7a0f6-131">Resurs-ID för HSM</span><span class="sxs-lookup"><span data-stu-id="7a0f6-131">HSM Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a0f6-132">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7a0f6-132">-Confirm</span></span>
<span data-ttu-id="7a0f6-133">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7a0f6-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a0f6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a0f6-134">-WhatIf</span></span>
<span data-ttu-id="7a0f6-135">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7a0f6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a0f6-136">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7a0f6-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a0f6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a0f6-137">CommonParameters</span></span>
<span data-ttu-id="7a0f6-138">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a0f6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a0f6-139">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a0f6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a0f6-140">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7a0f6-140">INPUTS</span></span>

### <span data-ttu-id="7a0f6-141">Microsoft. Azure. commands. valv. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7a0f6-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="7a0f6-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7a0f6-142">System.String</span></span>

## <span data-ttu-id="7a0f6-143">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7a0f6-143">OUTPUTS</span></span>

### <span data-ttu-id="7a0f6-144">Microsoft. Azure. commands. valv. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7a0f6-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="7a0f6-145">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7a0f6-145">NOTES</span></span>

## <span data-ttu-id="7a0f6-146">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7a0f6-146">RELATED LINKS</span></span>

[<span data-ttu-id="7a0f6-147">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="7a0f6-147">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="7a0f6-148">Säkerhets kopiering-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="7a0f6-148">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="7a0f6-149">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="7a0f6-149">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="7a0f6-150">Ångra-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="7a0f6-150">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="7a0f6-151">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="7a0f6-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="7a0f6-152">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="7a0f6-152">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)