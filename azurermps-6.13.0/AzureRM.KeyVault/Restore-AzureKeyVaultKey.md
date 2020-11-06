---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
ms.openlocfilehash: 70c56aaee4bf6547ad932965a190d3ecb2d93f6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574842"
---
# <span data-ttu-id="19cf8-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="19cf8-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="19cf8-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19cf8-102">SYNOPSIS</span></span>
<span data-ttu-id="19cf8-103">Skapar en nycklar i ett nyckelord från en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="19cf8-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19cf8-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19cf8-104">SYNTAX</span></span>

### <span data-ttu-id="19cf8-105">ByVaultName (standard)</span><span class="sxs-lookup"><span data-stu-id="19cf8-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19cf8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="19cf8-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19cf8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="19cf8-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultKey [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19cf8-108">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19cf8-108">DESCRIPTION</span></span>
<span data-ttu-id="19cf8-109">Cmdleten **restore-AzureKeyVaultKey** skapar en Key i det angivna nyckelvärdet.</span><span class="sxs-lookup"><span data-stu-id="19cf8-109">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="19cf8-110">Den här tangenten är en replik av säkerhets kopian i indatafilen och har samma namn som den ursprungliga tangenten.</span><span class="sxs-lookup"><span data-stu-id="19cf8-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="19cf8-111">Om det redan finns en nycklar med samma namn i nyckelordet kan denna cmdlet inte skriva över den ursprungliga tangenten.</span><span class="sxs-lookup"><span data-stu-id="19cf8-111">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="19cf8-112">Om säkerhets kopian innehåller flera versioner av en, återställs alla versioner.</span><span class="sxs-lookup"><span data-stu-id="19cf8-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="19cf8-113">Huvud valvet som du återställer nycklar till kan skilja sig från det viktiga valv som du säkerhetskopierade från.</span><span class="sxs-lookup"><span data-stu-id="19cf8-113">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="19cf8-114">Dessutom måste Key-valvet använda samma abonnemang och vara i ett Azure-område på samma geografi (till exempel Nord Amerika).</span><span class="sxs-lookup"><span data-stu-id="19cf8-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="19cf8-115">Se Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) för kart läggning av Azure-regioner till olika länder.</span><span class="sxs-lookup"><span data-stu-id="19cf8-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="19cf8-116">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19cf8-116">EXAMPLES</span></span>

### <span data-ttu-id="19cf8-117">Exempel 1: återställa en säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="19cf8-117">Example 1: Restore a backed-up key</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="19cf8-118">Det här kommandot återställer en nycklar, inklusive alla dess versioner, från säkerhets kopian med namnet Backup. blob till det nyckelord som heter MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="19cf8-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="19cf8-119">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19cf8-119">PARAMETERS</span></span>

### <span data-ttu-id="19cf8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19cf8-120">-DefaultProfile</span></span>
<span data-ttu-id="19cf8-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="19cf8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19cf8-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="19cf8-122">-InputFile</span></span>
<span data-ttu-id="19cf8-123">Anger den indatafil som innehåller säkerhets kopian av den fil som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="19cf8-123">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="19cf8-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19cf8-124">-InputObject</span></span>
<span data-ttu-id="19cf8-125">Valv objekt</span><span class="sxs-lookup"><span data-stu-id="19cf8-125">KeyVault object</span></span>

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

### <span data-ttu-id="19cf8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19cf8-126">-ResourceId</span></span>
<span data-ttu-id="19cf8-127">Resurs-ID för valv</span><span class="sxs-lookup"><span data-stu-id="19cf8-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="19cf8-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="19cf8-128">-VaultName</span></span>
<span data-ttu-id="19cf8-129">Anger namnet på det nyckelord som du vill återställa.</span><span class="sxs-lookup"><span data-stu-id="19cf8-129">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="19cf8-130">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="19cf8-130">-Confirm</span></span>
<span data-ttu-id="19cf8-131">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="19cf8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19cf8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19cf8-132">-WhatIf</span></span>
<span data-ttu-id="19cf8-133">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="19cf8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19cf8-134">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="19cf8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19cf8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19cf8-135">CommonParameters</span></span>
<span data-ttu-id="19cf8-136">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19cf8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19cf8-137">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19cf8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19cf8-138">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19cf8-138">INPUTS</span></span>

### <span data-ttu-id="19cf8-139">Microsoft. Azure. commands. valv. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="19cf8-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="19cf8-140">Parametrar: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="19cf8-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="19cf8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="19cf8-141">System.String</span></span>

## <span data-ttu-id="19cf8-142">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19cf8-142">OUTPUTS</span></span>

### <span data-ttu-id="19cf8-143">Microsoft. Azure. commands. valv. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="19cf8-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="19cf8-144">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19cf8-144">NOTES</span></span>

## <span data-ttu-id="19cf8-145">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19cf8-145">RELATED LINKS</span></span>

[<span data-ttu-id="19cf8-146">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="19cf8-146">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="19cf8-147">Säkerhets kopiering-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="19cf8-147">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="19cf8-148">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="19cf8-148">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="19cf8-149">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="19cf8-149">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

