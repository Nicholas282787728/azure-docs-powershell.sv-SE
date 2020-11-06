---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6E886340-864C-4FF6-8FA3-669D637770F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/disable-azurermbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
ms.openlocfilehash: ebea82628aae6df23d16a341f3fd503870a8037a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93582827"
---
# <span data-ttu-id="7fe01-101">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="7fe01-101">Disable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="7fe01-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="7fe01-102">SYNOPSIS</span></span>
<span data-ttu-id="7fe01-103">Inaktiverar skydd för ett skyddat objekt.</span><span class="sxs-lookup"><span data-stu-id="7fe01-103">Disables protection for a Backup protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fe01-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="7fe01-104">SYNTAX</span></span>

```
Disable-AzureRmBackupProtection [-RemoveRecoveryPoints] [-Force] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fe01-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="7fe01-105">DESCRIPTION</span></span>
<span data-ttu-id="7fe01-106">Cmdleten **disable-AzureRmBackupProtection** inaktiverar skyddet för ett skyddat Azure Backup-objekt.</span><span class="sxs-lookup"><span data-stu-id="7fe01-106">The **Disable-AzureRmBackupProtection** cmdlet disables protection for an Azure Backup protected item.</span></span>
<span data-ttu-id="7fe01-107">Denna cmdlet stoppar regelbunden schemalagd säkerhets kopiering av ett objekt.</span><span class="sxs-lookup"><span data-stu-id="7fe01-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="7fe01-108">Denna cmdlet kan ta bort befintliga återställnings punkter för säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="7fe01-108">This cmdlet can delete existing recovery points for the backup item.</span></span>

## <span data-ttu-id="7fe01-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="7fe01-109">EXAMPLES</span></span>

## <span data-ttu-id="7fe01-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="7fe01-110">PARAMETERS</span></span>

### <span data-ttu-id="7fe01-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fe01-111">-DefaultProfile</span></span>
<span data-ttu-id="7fe01-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="7fe01-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7fe01-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7fe01-113">-Force</span></span>
<span data-ttu-id="7fe01-114">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="7fe01-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7fe01-115">-Objekt</span><span class="sxs-lookup"><span data-stu-id="7fe01-115">-Item</span></span>
<span data-ttu-id="7fe01-116">Anger det säkerhets kopie objekt som denna cmdlet inaktiverar skydd för.</span><span class="sxs-lookup"><span data-stu-id="7fe01-116">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="7fe01-117">För att få en **AzureRmBackupItem** , Använd cmdleten Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="7fe01-117">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe01-118">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="7fe01-118">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="7fe01-119">Anger att den här cmdleten tar bort befintliga återställnings punkter.</span><span class="sxs-lookup"><span data-stu-id="7fe01-119">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="7fe01-120">Om du vill ta bort lagrade återställnings punkter senare kör du denna cmdlet igen och anger den här parametern.</span><span class="sxs-lookup"><span data-stu-id="7fe01-120">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fe01-121">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="7fe01-121">-Confirm</span></span>
<span data-ttu-id="7fe01-122">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="7fe01-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fe01-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fe01-123">-WhatIf</span></span>
<span data-ttu-id="7fe01-124">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="7fe01-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fe01-125">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="7fe01-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fe01-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fe01-126">CommonParameters</span></span>
<span data-ttu-id="7fe01-127">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fe01-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fe01-128">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fe01-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fe01-129">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="7fe01-129">INPUTS</span></span>

### <span data-ttu-id="7fe01-130">Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="7fe01-130">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>
<span data-ttu-id="7fe01-131">Parametrar: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7fe01-131">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="7fe01-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="7fe01-132">OUTPUTS</span></span>

### <span data-ttu-id="7fe01-133">Microsoft. Azure. commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="7fe01-133">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="7fe01-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="7fe01-134">NOTES</span></span>

## <span data-ttu-id="7fe01-135">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="7fe01-135">RELATED LINKS</span></span>

[<span data-ttu-id="7fe01-136">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="7fe01-136">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="7fe01-137">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="7fe01-137">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)


