---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 17a39152c6e341773a2c3db7b701e0d37890f110
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94263013"
---
# <span data-ttu-id="adcb0-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="adcb0-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="adcb0-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="adcb0-102">SYNOPSIS</span></span>
<span data-ttu-id="adcb0-103">Skapar en nycklar i ett nyckelord från en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="adcb0-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="adcb0-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="adcb0-104">SYNTAX</span></span>

### <span data-ttu-id="adcb0-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="adcb0-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adcb0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="adcb0-106">ByInputObject</span></span>
```
Restore-AzKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adcb0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="adcb0-107">ByResourceId</span></span>
```
Restore-AzKeyVaultKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adcb0-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="adcb0-108">DESCRIPTION</span></span>
<span data-ttu-id="adcb0-109">Cmdleten **restore-AzKeyVaultKey** skapar en Key i det angivna nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="adcb0-109">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="adcb0-110">Den här tangenten är en replik av säkerhets kopian i indatafilen och har samma namn som den ursprungliga tangenten.</span><span class="sxs-lookup"><span data-stu-id="adcb0-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="adcb0-111">Om det redan finns en nycklar med samma namn i nyckelordet kan denna cmdlet inte skriva över den ursprungliga tangenten.</span><span class="sxs-lookup"><span data-stu-id="adcb0-111">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="adcb0-112">Om säkerhets kopian innehåller flera versioner av en, återställs alla versioner.</span><span class="sxs-lookup"><span data-stu-id="adcb0-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="adcb0-113">Huvud valvet som du återställer nycklar till kan skilja sig från det viktiga valv som du säkerhetskopierade från.</span><span class="sxs-lookup"><span data-stu-id="adcb0-113">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="adcb0-114">Dessutom måste Key-valvet använda samma abonnemang och vara i ett Azure-område på samma geografi (till exempel Nord Amerika).</span><span class="sxs-lookup"><span data-stu-id="adcb0-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="adcb0-115">Se Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) för kart läggning av Azure-regioner till olika länder.</span><span class="sxs-lookup"><span data-stu-id="adcb0-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="adcb0-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="adcb0-116">EXAMPLES</span></span>

### <span data-ttu-id="adcb0-117">Exempel 1: återställa en säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="adcb0-117">Example 1: Restore a backed-up key</span></span>
```powershell
PS C:\> Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Vault Name     : MyKeyVault
Name           : key1
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://mykeyvault.vault.azure.net:443/keys/key1/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        :
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 4/6/2018 11:35:04 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="adcb0-118">Det här kommandot återställer en nycklar, inklusive alla dess versioner, från säkerhets kopian med namnet Backup. blob till det nyckelord som heter MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="adcb0-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="adcb0-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="adcb0-119">PARAMETERS</span></span>

### <span data-ttu-id="adcb0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adcb0-120">-DefaultProfile</span></span>
<span data-ttu-id="adcb0-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="adcb0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adcb0-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="adcb0-122">-InputFile</span></span>
<span data-ttu-id="adcb0-123">Anger den indatafil som innehåller säkerhets kopian av den fil som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="adcb0-123">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="adcb0-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adcb0-124">-InputObject</span></span>
<span data-ttu-id="adcb0-125">Valv objekt</span><span class="sxs-lookup"><span data-stu-id="adcb0-125">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adcb0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adcb0-126">-ResourceId</span></span>
<span data-ttu-id="adcb0-127">Resurs-ID för valv</span><span class="sxs-lookup"><span data-stu-id="adcb0-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="adcb0-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="adcb0-128">-VaultName</span></span>
<span data-ttu-id="adcb0-129">Anger namnet på det nyckelord som du vill återställa.</span><span class="sxs-lookup"><span data-stu-id="adcb0-129">Specifies the name of the key vault into which to restore the key.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adcb0-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="adcb0-130">-Confirm</span></span>
<span data-ttu-id="adcb0-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="adcb0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adcb0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adcb0-132">-WhatIf</span></span>
<span data-ttu-id="adcb0-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="adcb0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adcb0-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="adcb0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adcb0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adcb0-135">CommonParameters</span></span>
<span data-ttu-id="adcb0-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adcb0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adcb0-137">Mer information finns i [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="adcb0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adcb0-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="adcb0-138">INPUTS</span></span>

### <span data-ttu-id="adcb0-139">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="adcb0-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="adcb0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="adcb0-140">System.String</span></span>

## <span data-ttu-id="adcb0-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="adcb0-141">OUTPUTS</span></span>

### <span data-ttu-id="adcb0-142">Microsoft. Azure. commands. valv. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="adcb0-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="adcb0-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="adcb0-143">NOTES</span></span>

## <span data-ttu-id="adcb0-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="adcb0-144">RELATED LINKS</span></span>

[<span data-ttu-id="adcb0-145">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="adcb0-145">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="adcb0-146">Säkerhets kopiering-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="adcb0-146">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="adcb0-147">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="adcb0-147">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="adcb0-148">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="adcb0-148">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)
