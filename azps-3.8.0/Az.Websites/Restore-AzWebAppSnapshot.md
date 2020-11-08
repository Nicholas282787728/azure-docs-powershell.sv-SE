---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppSnapshot.md
ms.openlocfilehash: 1dd84305753edc8ad639c160c9003c4c393d041e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94090625"
---
# <span data-ttu-id="4d939-101">Restore-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="4d939-101">Restore-AzWebAppSnapshot</span></span>

## <span data-ttu-id="4d939-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="4d939-102">SYNOPSIS</span></span>
<span data-ttu-id="4d939-103">Återställer en webb programs stillbild.</span><span class="sxs-lookup"><span data-stu-id="4d939-103">Restores a web app snapshot.</span></span>

## <span data-ttu-id="4d939-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="4d939-104">SYNTAX</span></span>

### <span data-ttu-id="4d939-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="4d939-105">FromResourceName</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d939-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="4d939-106">FromWebApp</span></span>
```
Restore-AzWebAppSnapshot [-RecoverConfiguration] [-UseDisasterRecovery] [-Force] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d939-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="4d939-107">DESCRIPTION</span></span>
<span data-ttu-id="4d939-108">Återställer en webb programs stillbild till webb programmet.</span><span class="sxs-lookup"><span data-stu-id="4d939-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="4d939-109">Om du återställer en ögonblicks bild skrivs alla filer i ett webbprogram till med de filer som finns i ögonblicks bilden.</span><span class="sxs-lookup"><span data-stu-id="4d939-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="4d939-110">Om du vill återställa inställningarna kan du använda växeln RecoverConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4d939-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="4d939-111">En ögonblicks bild från en webbapp kan återställas till alla andra webbappar i samma prenumeration.</span><span class="sxs-lookup"><span data-stu-id="4d939-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="4d939-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="4d939-112">EXAMPLES</span></span>

### <span data-ttu-id="4d939-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="4d939-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="4d939-114">Hämtar den senaste ögonblicks bilden av ett webb program med namnet "ContosoApp" med en plats med namnet "mellanlagring" i resurs gruppen "default-Web-West".</span><span class="sxs-lookup"><span data-stu-id="4d939-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="4d939-115">Återställer ögonblicks bilden till webb programmets "Återställ"-fack.</span><span class="sxs-lookup"><span data-stu-id="4d939-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="4d939-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="4d939-116">PARAMETERS</span></span>

### <span data-ttu-id="4d939-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d939-117">-AsJob</span></span>
<span data-ttu-id="4d939-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="4d939-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4d939-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d939-119">-DefaultProfile</span></span>
<span data-ttu-id="4d939-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="4d939-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d939-121">-Force</span><span class="sxs-lookup"><span data-stu-id="4d939-121">-Force</span></span>
<span data-ttu-id="4d939-122">Tillåter att det ursprungliga webb programmet skrivs över utan att en varning visas.</span><span class="sxs-lookup"><span data-stu-id="4d939-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d939-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d939-123">-InputObject</span></span>
<span data-ttu-id="4d939-124">Ögonblicks bild av Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="4d939-124">The Azure Web App snapshot.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d939-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="4d939-125">-Name</span></span>
<span data-ttu-id="4d939-126">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="4d939-126">The name of the web app.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d939-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d939-127">-RecoverConfiguration</span></span>
<span data-ttu-id="4d939-128">Återställ webb programmets konfiguration i tillägg till filer.</span><span class="sxs-lookup"><span data-stu-id="4d939-128">Recover the web app's configuration in addition to files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d939-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d939-129">-ResourceGroupName</span></span>
<span data-ttu-id="4d939-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="4d939-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d939-131">-Plats</span><span class="sxs-lookup"><span data-stu-id="4d939-131">-Slot</span></span>
<span data-ttu-id="4d939-132">Namnet på Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="4d939-132">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d939-133">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="4d939-133">-UseDisasterRecovery</span></span>
<span data-ttu-id="4d939-134">Använd det här alternativet om du vill återställa en ögonblicks bild från en enhet som är offline.</span><span class="sxs-lookup"><span data-stu-id="4d939-134">Use to recover a snapshot from a scale unit that is offline.</span></span>

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

### <span data-ttu-id="4d939-135">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4d939-135">-WebApp</span></span>
<span data-ttu-id="4d939-136">Web App-objekt</span><span class="sxs-lookup"><span data-stu-id="4d939-136">The web app object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d939-137">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="4d939-137">-Confirm</span></span>
<span data-ttu-id="4d939-138">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="4d939-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d939-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d939-139">-WhatIf</span></span>
<span data-ttu-id="4d939-140">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="4d939-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d939-141">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="4d939-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d939-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d939-142">CommonParameters</span></span>
<span data-ttu-id="4d939-143">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d939-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d939-144">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d939-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d939-145">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="4d939-145">INPUTS</span></span>

### <span data-ttu-id="4d939-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4d939-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="4d939-147">System. String</span><span class="sxs-lookup"><span data-stu-id="4d939-147">System.String</span></span>

### <span data-ttu-id="4d939-148">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="4d939-148">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="4d939-149">Microsoft. Azure. kommandon. webapps. cmdletar. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="4d939-149">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="4d939-150">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="4d939-150">OUTPUTS</span></span>

### <span data-ttu-id="4d939-151">System. Void</span><span class="sxs-lookup"><span data-stu-id="4d939-151">System.Void</span></span>

## <span data-ttu-id="4d939-152">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="4d939-152">NOTES</span></span>

## <span data-ttu-id="4d939-153">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="4d939-153">RELATED LINKS</span></span>
