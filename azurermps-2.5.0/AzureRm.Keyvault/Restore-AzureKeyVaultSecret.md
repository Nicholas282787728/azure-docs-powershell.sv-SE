---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: b8ce1dc13204cfeeb63f5b7eb45f57e2117da511
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928777"
---
# <span data-ttu-id="ea454-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ea454-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="ea454-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ea454-102">SYNOPSIS</span></span>
<span data-ttu-id="ea454-103">Skapar en hemlighet i ett nyckel valv från en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="ea454-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea454-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ea454-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea454-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ea454-105">DESCRIPTION</span></span>
<span data-ttu-id="ea454-106">Cmdleten **restore-AzureKeyVaultSecret** skapar en hemlighet i det angivna nyckel valvet.</span><span class="sxs-lookup"><span data-stu-id="ea454-106">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="ea454-107">Denna hemlighet är en replik av den säkerhetskopierade hemligheten i indatafilen och har samma namn som den ursprungliga hemligheten.</span><span class="sxs-lookup"><span data-stu-id="ea454-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="ea454-108">Om nyckel valvet redan har en hemlighet med samma namn, Miss lyckas denna cmdlet i stället för att skriva över den ursprungliga hemligheten.</span><span class="sxs-lookup"><span data-stu-id="ea454-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="ea454-109">Om säkerhets kopian innehåller flera versioner av en hemlighet återställs alla versioner.</span><span class="sxs-lookup"><span data-stu-id="ea454-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="ea454-110">Nyckel valvet som du återställer hemligheten till kan skilja sig från det nyckel valv som du säkerhetskopierade hemligheten från.</span><span class="sxs-lookup"><span data-stu-id="ea454-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="ea454-111">Dessutom måste Key-valvet använda samma abonnemang och vara i ett Azure-område på samma geografi (till exempel Nord Amerika).</span><span class="sxs-lookup"><span data-stu-id="ea454-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="ea454-112">Se Microsoft Azure Trust Center ( https://azure.microsoft.com/support/trust-center/) för kart läggning av Azure-regioner till olika länder.</span><span class="sxs-lookup"><span data-stu-id="ea454-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="ea454-113">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ea454-113">EXAMPLES</span></span>

### <span data-ttu-id="ea454-114">Exempel 1: återställa en säkerhets kopia</span><span class="sxs-lookup"><span data-stu-id="ea454-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="ea454-115">Det här kommandot återställer en hemlighet, inklusive alla dess versioner, från säkerhets kopian med namnet Backup. blob till nyckel valvet med namnet MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="ea454-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="ea454-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ea454-116">PARAMETERS</span></span>

### <span data-ttu-id="ea454-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea454-117">-DefaultProfile</span></span>
<span data-ttu-id="ea454-118">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="ea454-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea454-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="ea454-119">-InputFile</span></span>
<span data-ttu-id="ea454-120">Anger den indatafil som innehåller säkerhets kopian av hemligheten som ska återställas.</span><span class="sxs-lookup"><span data-stu-id="ea454-120">Specifies the input file that contains the backup of the secret to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea454-121">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ea454-121">-VaultName</span></span>
<span data-ttu-id="ea454-122">Anger namnet på det nyckel valv som du vill återställa hemligheten till.</span><span class="sxs-lookup"><span data-stu-id="ea454-122">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="ea454-123">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ea454-123">-Confirm</span></span>
<span data-ttu-id="ea454-124">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ea454-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea454-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea454-125">-WhatIf</span></span>
<span data-ttu-id="ea454-126">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ea454-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea454-127">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ea454-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea454-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea454-128">CommonParameters</span></span>
<span data-ttu-id="ea454-129">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea454-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea454-130">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea454-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea454-131">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ea454-131">INPUTS</span></span>

## <span data-ttu-id="ea454-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ea454-132">OUTPUTS</span></span>

### <span data-ttu-id="ea454-133">Microsoft. Azure. commands. nyckel valv. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="ea454-133">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="ea454-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ea454-134">NOTES</span></span>

## <span data-ttu-id="ea454-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ea454-135">RELATED LINKS</span></span>

[<span data-ttu-id="ea454-136">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ea454-136">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="ea454-137">Säkerhets kopiering-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ea454-137">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="ea454-138">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ea454-138">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="ea454-139">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ea454-139">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

