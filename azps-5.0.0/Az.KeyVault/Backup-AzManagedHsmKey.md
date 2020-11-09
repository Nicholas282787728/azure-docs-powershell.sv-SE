---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
ms.openlocfilehash: 9e75b6de483f0103103434518d31b472660f4a70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319916"
---
# <span data-ttu-id="08241-101">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="08241-101">Backup-AzManagedHsmKey</span></span>

## <span data-ttu-id="08241-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="08241-102">SYNOPSIS</span></span>
<span data-ttu-id="08241-103">Säkerhetskopierar en nycklar i en hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="08241-103">Backs up a key in a managed HSM.</span></span>

## <span data-ttu-id="08241-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="08241-104">SYNTAX</span></span>

### <span data-ttu-id="08241-105">ByKeyName (standard)</span><span class="sxs-lookup"><span data-stu-id="08241-105">ByKeyName (Default)</span></span>
```
Backup-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08241-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="08241-106">ByKey</span></span>
```
Backup-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08241-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="08241-107">DESCRIPTION</span></span>
<span data-ttu-id="08241-108">**Säkerhets kopiering-AzManagedHsmKey** cmdlet återställer en specifik server i en hanterad HSM genom att hämta den och lagra den i en fil.</span><span class="sxs-lookup"><span data-stu-id="08241-108">The **Backup-AzManagedHsmKey** cmdlet backs up a specified key in a managed HSM by downloading it and storing it in a file.</span></span>
<span data-ttu-id="08241-109">Om det finns flera versioner av nycklarna är alla versioner inkluderade i säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="08241-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="08241-110">Eftersom det hämtade innehållet är krypterat kan det inte användas utanför Azure Managed HSM.</span><span class="sxs-lookup"><span data-stu-id="08241-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Managed HSM.</span></span>
<span data-ttu-id="08241-111">Du kan återställa en säkerhets kopie rad server till valfri hanterad HSM i det abonnemang som den säkerhetskopierades från.</span><span class="sxs-lookup"><span data-stu-id="08241-111">You can restore a backed-up key to any managed HSM in the subscription that it was backed up from.</span></span>
<span data-ttu-id="08241-112">Vanliga skäl till att använda denna cmdlet är:</span><span class="sxs-lookup"><span data-stu-id="08241-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="08241-113">Du vill Escrow en kopia av dina nycklar så att du har en offlinekopia ifall du råkar ta bort den från hanterad HSM.</span><span class="sxs-lookup"><span data-stu-id="08241-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your managed HSM.</span></span>
 
- <span data-ttu-id="08241-114">Du har skapat en server med hanterad HSM och vill nu klona tangenten till ett annat Azure-område, så att du kan använda den från alla instanser av det distribuerade programmet.</span><span class="sxs-lookup"><span data-stu-id="08241-114">You created a key using Managed HSM and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="08241-115">Använd **säkerhets kopierings-AzManagedHsmKey** cmdlet för att hämta nycklar i krypterat format och använd sedan Restore-AzManagedHsmKey cmdlet och ange en hanterad HSM i den andra regionen.</span><span class="sxs-lookup"><span data-stu-id="08241-115">Use the **Backup-AzManagedHsmKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzManagedHsmKey cmdlet and specify a managed HSM in the second region.</span></span>

## <span data-ttu-id="08241-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="08241-116">EXAMPLES</span></span>

### <span data-ttu-id="08241-117">Exempel 1: säkerhetskopiera en nycklar med ett automatiskt genererat fil namn</span><span class="sxs-lookup"><span data-stu-id="08241-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzManagedHsmKey -HsmName testmhsm -Name testkey

C:\Users\username\testmhsm-testkey-1602664728.7106073
```

<span data-ttu-id="08241-118">Det här kommandot hämtar den nycklar som heter testkey från den hanterade HSM som heter testmhsm och sparar en säkerhets kopia av den till en fil som automatiskt namnges för dig och visar fil namnet.</span><span class="sxs-lookup"><span data-stu-id="08241-118">This command retrieves the key named testkey from the managed HSM named testmhsm and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

## <span data-ttu-id="08241-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="08241-119">PARAMETERS</span></span>

### <span data-ttu-id="08241-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08241-120">-DefaultProfile</span></span>
<span data-ttu-id="08241-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="08241-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08241-122">-Force</span><span class="sxs-lookup"><span data-stu-id="08241-122">-Force</span></span>
<span data-ttu-id="08241-123">Skriv över den angivna filen om den finns</span><span class="sxs-lookup"><span data-stu-id="08241-123">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="08241-124">-HsmName</span><span class="sxs-lookup"><span data-stu-id="08241-124">-HsmName</span></span>
<span data-ttu-id="08241-125">HSM-namn.</span><span class="sxs-lookup"><span data-stu-id="08241-125">HSM name.</span></span> <span data-ttu-id="08241-126">Cmdlet konstruerar FQDN för en hanterad HSM baserat på namnet och den valda miljön.</span><span class="sxs-lookup"><span data-stu-id="08241-126">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08241-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08241-127">-InputObject</span></span>
<span data-ttu-id="08241-128">Huvud paket att säkerhetskopiera från utdata från ett samtal.</span><span class="sxs-lookup"><span data-stu-id="08241-128">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08241-129">-Namn</span><span class="sxs-lookup"><span data-stu-id="08241-129">-Name</span></span>
<span data-ttu-id="08241-130">Namn på knappen.</span><span class="sxs-lookup"><span data-stu-id="08241-130">Key name.</span></span>
<span data-ttu-id="08241-131">Cmdlet konstruerar FQDN för en Key från Managed HSM-namn, markerat miljö-och namn för tillfället.</span><span class="sxs-lookup"><span data-stu-id="08241-131">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08241-132">-Utdatafil</span><span class="sxs-lookup"><span data-stu-id="08241-132">-OutputFile</span></span>
<span data-ttu-id="08241-133">Utdatafil.</span><span class="sxs-lookup"><span data-stu-id="08241-133">Output file.</span></span>
<span data-ttu-id="08241-134">Utdatafil som den säkerhetskopierade BLOB-blobben lagras i.</span><span class="sxs-lookup"><span data-stu-id="08241-134">The output file to store the backed up key blob in.</span></span>
<span data-ttu-id="08241-135">Om det inte finns något är standard fil namnet markerat.</span><span class="sxs-lookup"><span data-stu-id="08241-135">If not present, a default filename is chosen.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08241-136">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="08241-136">-Confirm</span></span>
<span data-ttu-id="08241-137">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="08241-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08241-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08241-138">-WhatIf</span></span>
<span data-ttu-id="08241-139">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="08241-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08241-140">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="08241-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08241-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08241-141">CommonParameters</span></span>
<span data-ttu-id="08241-142">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08241-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08241-143">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08241-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08241-144">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="08241-144">INPUTS</span></span>

### <span data-ttu-id="08241-145">Microsoft. Azure. commands. valv. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="08241-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="08241-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="08241-146">OUTPUTS</span></span>

### <span data-ttu-id="08241-147">System. String</span><span class="sxs-lookup"><span data-stu-id="08241-147">System.String</span></span>

## <span data-ttu-id="08241-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="08241-148">NOTES</span></span>

## <span data-ttu-id="08241-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="08241-149">RELATED LINKS</span></span>

[<span data-ttu-id="08241-150">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="08241-150">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="08241-151">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="08241-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="08241-152">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="08241-152">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="08241-153">Ångra-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="08241-153">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="08241-154">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="08241-154">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="08241-155">Återställ-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="08241-155">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)