---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35b937b810da65cc3cc2ed330198011ec108f9d6
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 05/19/2020
ms.locfileid: "93928278"
---
# <span data-ttu-id="e29f9-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="e29f9-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="e29f9-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e29f9-102">SYNOPSIS</span></span>
<span data-ttu-id="e29f9-103">Återställa en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="e29f9-103">Restore a backup.</span></span>

## <span data-ttu-id="e29f9-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e29f9-104">SYNTAX</span></span>

### <span data-ttu-id="e29f9-105">Backups_Restore (standard)</span><span class="sxs-lookup"><span data-stu-id="e29f9-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>]
 -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e29f9-106">ID</span><span class="sxs-lookup"><span data-stu-id="e29f9-106">ResourceId</span></span>
```
Restore-AzsBackup -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e29f9-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e29f9-107">DESCRIPTION</span></span>
<span data-ttu-id="e29f9-108">Återställa en säkerhets kopia.</span><span class="sxs-lookup"><span data-stu-id="e29f9-108">Restore a backup.</span></span>

## <span data-ttu-id="e29f9-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e29f9-109">EXAMPLES</span></span>

### <span data-ttu-id="e29f9-110">EXEMPEL 1</span><span class="sxs-lookup"><span data-stu-id="e29f9-110">EXAMPLE 1</span></span>
```
Restore-AzsBackup -Name 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword
```

<span data-ttu-id="e29f9-111">Återställ från en Azure Stack-säkerhetskopia.</span><span class="sxs-lookup"><span data-stu-id="e29f9-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="e29f9-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e29f9-112">PARAMETERS</span></span>

### <span data-ttu-id="e29f9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e29f9-113">-AsJob</span></span>
<span data-ttu-id="e29f9-114">Kör asynkront som ett jobb och returnera jobbobjektet.</span><span class="sxs-lookup"><span data-stu-id="e29f9-114">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29f9-115">-DecryptionCertPassword</span><span class="sxs-lookup"><span data-stu-id="e29f9-115">-DecryptionCertPassword</span></span>
<span data-ttu-id="e29f9-116">Lösen ordet för det avkrypterade certifikatet.</span><span class="sxs-lookup"><span data-stu-id="e29f9-116">Password of the decryption cert.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29f9-117">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="e29f9-117">-DecryptionCertPath</span></span>
<span data-ttu-id="e29f9-118">Sökväg till dekrypteringsnyckeln med en privat nyckel (. pfx).</span><span class="sxs-lookup"><span data-stu-id="e29f9-118">Path to the decryption cert file with private key (.pfx).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29f9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e29f9-119">-Force</span></span>
<span data-ttu-id="e29f9-120">Fråga inte efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="e29f9-120">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29f9-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="e29f9-121">-Location</span></span>
<span data-ttu-id="e29f9-122">Namn på plats för säkerhets kopiering.</span><span class="sxs-lookup"><span data-stu-id="e29f9-122">Name of location to backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29f9-123">-Namn</span><span class="sxs-lookup"><span data-stu-id="e29f9-123">-Name</span></span>
<span data-ttu-id="e29f9-124">Namn på säkerhets kopian.</span><span class="sxs-lookup"><span data-stu-id="e29f9-124">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29f9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e29f9-125">-ResourceGroupName</span></span>
<span data-ttu-id="e29f9-126">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="e29f9-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e29f9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e29f9-127">-ResourceId</span></span>
<span data-ttu-id="e29f9-128">Resurs-ID.</span><span class="sxs-lookup"><span data-stu-id="e29f9-128">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e29f9-129">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e29f9-129">-Confirm</span></span>
<span data-ttu-id="e29f9-130">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e29f9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e29f9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e29f9-131">-WhatIf</span></span>
<span data-ttu-id="e29f9-132">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e29f9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e29f9-133">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e29f9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e29f9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e29f9-134">CommonParameters</span></span>
<span data-ttu-id="e29f9-135">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e29f9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e29f9-136">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e29f9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e29f9-137">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e29f9-137">INPUTS</span></span>

## <span data-ttu-id="e29f9-138">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e29f9-138">OUTPUTS</span></span>

## <span data-ttu-id="e29f9-139">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e29f9-139">NOTES</span></span>

## <span data-ttu-id="e29f9-140">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e29f9-140">RELATED LINKS</span></span>
