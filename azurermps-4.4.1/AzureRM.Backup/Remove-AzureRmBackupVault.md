---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 698DCD00-13C0-4C36-A74B-35215D608339
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
ms.openlocfilehash: 8530dbff2e348f1b068afe7293cae9c993ce064e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93578496"
---
# <span data-ttu-id="ef834-101">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ef834-101">Remove-AzureRmBackupVault</span></span>

## <span data-ttu-id="ef834-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="ef834-102">SYNOPSIS</span></span>
<span data-ttu-id="ef834-103">Tar bort ett säkerhets kopierings valv.</span><span class="sxs-lookup"><span data-stu-id="ef834-103">Deletes a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef834-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="ef834-104">SYNTAX</span></span>

```
Remove-AzureRmBackupVault [-Force] [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef834-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="ef834-105">DESCRIPTION</span></span>
<span data-ttu-id="ef834-106">Cmdleten **Remove-AzureRmBackupVault** tar bort ett Azure Backup-valv.</span><span class="sxs-lookup"><span data-stu-id="ef834-106">The **Remove-AzureRmBackupVault** cmdlet deletes an Azure Backup vault.</span></span>

<span data-ttu-id="ef834-107">Innan du kan ta bort ett säkerhets kopierings valv måste det vara tomt.</span><span class="sxs-lookup"><span data-stu-id="ef834-107">Before you can delete a Backup vault, it must be empty.</span></span>
<span data-ttu-id="ef834-108">Använd cmdleten **Remove-AzureRmBackupContainer** för att ta bort infrastrukturen som en tjänst (IaaS) säkerhets kopiering av data från valvet.</span><span class="sxs-lookup"><span data-stu-id="ef834-108">Use the **Remove-AzureRmBackupContainer** cmdlet to remove infrastructure as a service (IaaS) virtual machine backup data from the vault.</span></span>
<span data-ttu-id="ef834-109">Använd cmdleten **Delete-RegisteredServer** för att ta bort andra registrerade servrar och säkerhets kopior.</span><span class="sxs-lookup"><span data-stu-id="ef834-109">Use the **Delete-RegisteredServer** cmdlet to remove other registered servers and backup data.</span></span>

## <span data-ttu-id="ef834-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="ef834-110">EXAMPLES</span></span>

### <span data-ttu-id="ef834-111">Exempel 1: ta bort ett Azure Backup-valv</span><span class="sxs-lookup"><span data-stu-id="ef834-111">Example 1: Delete an Azure Backup vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Remove-AzureRmBackupVault
```

<span data-ttu-id="ef834-112">Det här kommandot får Azure Backup-valvet med namnet Vault03 med hjälp av cmdleten **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="ef834-112">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="ef834-113">Kommandot skickar detta valv till den aktuella cmdleten med hjälp av pipeline-operatorn.</span><span class="sxs-lookup"><span data-stu-id="ef834-113">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ef834-114">Den aktuella cmdleten tar bort valvet.</span><span class="sxs-lookup"><span data-stu-id="ef834-114">The current cmdlet removes the vault.</span></span>

## <span data-ttu-id="ef834-115">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="ef834-115">PARAMETERS</span></span>

### <span data-ttu-id="ef834-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ef834-116">-Force</span></span>
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

### <span data-ttu-id="ef834-117">-Valv</span><span class="sxs-lookup"><span data-stu-id="ef834-117">-Vault</span></span>
<span data-ttu-id="ef834-118">Anger ett säkerhets kopierings valv som denna cmdlet tar bort.</span><span class="sxs-lookup"><span data-stu-id="ef834-118">Specifies a Backup vault that this cmdlet removes.</span></span>
<span data-ttu-id="ef834-119">För att få en **AzureRmBackupVault** , Använd cmdleten Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="ef834-119">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef834-120">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="ef834-120">-Confirm</span></span>
<span data-ttu-id="ef834-121">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="ef834-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef834-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef834-122">-WhatIf</span></span>
<span data-ttu-id="ef834-123">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="ef834-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef834-124">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="ef834-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef834-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef834-125">-DefaultProfile</span></span>
<span data-ttu-id="ef834-126">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="ef834-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef834-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef834-127">CommonParameters</span></span>
<span data-ttu-id="ef834-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef834-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef834-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef834-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef834-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="ef834-130">INPUTS</span></span>

### <span data-ttu-id="ef834-131">AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="ef834-131">AzureRMBackupVault</span></span>

## <span data-ttu-id="ef834-132">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="ef834-132">OUTPUTS</span></span>

### <span data-ttu-id="ef834-133">Ingen</span><span class="sxs-lookup"><span data-stu-id="ef834-133">None</span></span>

## <span data-ttu-id="ef834-134">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="ef834-134">NOTES</span></span>
* <span data-ttu-id="ef834-135">Ingen</span><span class="sxs-lookup"><span data-stu-id="ef834-135">None</span></span>

## <span data-ttu-id="ef834-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="ef834-136">RELATED LINKS</span></span>

[<span data-ttu-id="ef834-137">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ef834-137">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="ef834-138">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ef834-138">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="ef834-139">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="ef834-139">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


