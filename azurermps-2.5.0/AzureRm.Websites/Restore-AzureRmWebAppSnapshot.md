---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappsnapshot
schema: 2.0.0
ms.openlocfilehash: 0719210cae275dc7e250e7fd14e622c51014d7c2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93930781"
---
# <span data-ttu-id="bd72c-101">Restore-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="bd72c-101">Restore-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="bd72c-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="bd72c-102">SYNOPSIS</span></span>
<span data-ttu-id="bd72c-103">Återställer en webb programs stillbild.</span><span class="sxs-lookup"><span data-stu-id="bd72c-103">Restores a web app snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd72c-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="bd72c-104">SYNTAX</span></span>

### <span data-ttu-id="bd72c-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="bd72c-105">FromResourceName</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-ResourceGroupName] <String>
 [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd72c-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="bd72c-106">FromWebApp</span></span>
```
Restore-AzureRmWebAppSnapshot [-RecoverConfiguration] [-Force] [-AsJob] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-InputObject] <AzureWebAppSnapshot> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd72c-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="bd72c-107">DESCRIPTION</span></span>
<span data-ttu-id="bd72c-108">Återställer en webb programs stillbild till webb programmet.</span><span class="sxs-lookup"><span data-stu-id="bd72c-108">Restores a web app snapshot to the web app.</span></span> <span data-ttu-id="bd72c-109">Om du återställer en ögonblicks bild skrivs alla filer i ett webbprogram till med de filer som finns i ögonblicks bilden.</span><span class="sxs-lookup"><span data-stu-id="bd72c-109">Restoring a snapshot overwrites all files in a web app with the files contained in the snapshot.</span></span> <span data-ttu-id="bd72c-110">Om du vill återställa inställningarna kan du använda växeln RecoverConfiguration.</span><span class="sxs-lookup"><span data-stu-id="bd72c-110">To restore settings as well, use the RecoverConfiguration switch parameter.</span></span> <span data-ttu-id="bd72c-111">En ögonblicks bild från en webbapp kan återställas till alla andra webbappar i samma prenumeration.</span><span class="sxs-lookup"><span data-stu-id="bd72c-111">A snapshot from one web app can be restored to any other web app in the same subscription.</span></span>

## <span data-ttu-id="bd72c-112">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="bd72c-112">EXAMPLES</span></span>

### <span data-ttu-id="bd72c-113">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="bd72c-113">Example 1</span></span>
```
PS C:\> $snapshot = (Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging")[0]
PS C:\> Restore-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Restore" -InputObject $snapshot -RecoverConfiguration
```

<span data-ttu-id="bd72c-114">Hämtar den senaste ögonblicks bilden av ett webb program med namnet "ContosoApp" med en plats med namnet "mellanlagring" i resurs gruppen "default-Web-West".</span><span class="sxs-lookup"><span data-stu-id="bd72c-114">Gets the latest snapshot of a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group.</span></span> <span data-ttu-id="bd72c-115">Återställer ögonblicks bilden till webb programmets "Återställ"-fack.</span><span class="sxs-lookup"><span data-stu-id="bd72c-115">Restores the snapshot to the web app's "Restore" slot.</span></span>

## <span data-ttu-id="bd72c-116">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="bd72c-116">PARAMETERS</span></span>

### <span data-ttu-id="bd72c-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd72c-117">-AsJob</span></span>
<span data-ttu-id="bd72c-118">Kör cmdlet i bakgrunden</span><span class="sxs-lookup"><span data-stu-id="bd72c-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd72c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd72c-119">-DefaultProfile</span></span>
<span data-ttu-id="bd72c-120">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="bd72c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd72c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bd72c-121">-Force</span></span>
<span data-ttu-id="bd72c-122">Tillåter att det ursprungliga webb programmet skrivs över utan att en varning visas.</span><span class="sxs-lookup"><span data-stu-id="bd72c-122">Allows the original web app to be overwritten without displaying a warning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd72c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd72c-123">-InputObject</span></span>
<span data-ttu-id="bd72c-124">Ögonblicks bild av Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="bd72c-124">The Azure Web App snapshot.</span></span>
```yaml
Type: AzureWebAppSnapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd72c-125">-Namn</span><span class="sxs-lookup"><span data-stu-id="bd72c-125">-Name</span></span>
<span data-ttu-id="bd72c-126">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="bd72c-126">The name of the web app.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd72c-127">-RecoverConfiguration</span><span class="sxs-lookup"><span data-stu-id="bd72c-127">-RecoverConfiguration</span></span>
<span data-ttu-id="bd72c-128">Återställ webb programmets konfiguration i tillägg till filer.</span><span class="sxs-lookup"><span data-stu-id="bd72c-128">Recover the web app's configuration in addition to files.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd72c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd72c-129">-ResourceGroupName</span></span>
<span data-ttu-id="bd72c-130">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="bd72c-130">The name of the resource group.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd72c-131">-Plats</span><span class="sxs-lookup"><span data-stu-id="bd72c-131">-Slot</span></span>
<span data-ttu-id="bd72c-132">Namnet på Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="bd72c-132">The name of the web app slot.</span></span>
```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd72c-133">-WebApp</span><span class="sxs-lookup"><span data-stu-id="bd72c-133">-WebApp</span></span>
<span data-ttu-id="bd72c-134">Web App-objekt</span><span class="sxs-lookup"><span data-stu-id="bd72c-134">The web app object</span></span>
```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd72c-135">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="bd72c-135">-Confirm</span></span>
<span data-ttu-id="bd72c-136">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="bd72c-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd72c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd72c-137">-WhatIf</span></span>
<span data-ttu-id="bd72c-138">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="bd72c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd72c-139">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="bd72c-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd72c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd72c-140">CommonParameters</span></span>
<span data-ttu-id="bd72c-141">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd72c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd72c-142">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd72c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd72c-143">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="bd72c-143">INPUTS</span></span>

### <span data-ttu-id="bd72c-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bd72c-144">System.Management.Automation.SwitchParameter</span></span>
<span data-ttu-id="bd72c-145">Microsoft. Azure. Management. sites. Models. webbplats system. String Microsoft. Azure. kommandon. webapps. cmdletar. BackupRestore. AzureWebAppSnapshot system. DateTime</span><span class="sxs-lookup"><span data-stu-id="bd72c-145">Microsoft.Azure.Management.WebSites.Models.Site System.String Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot System.DateTime</span></span>

## <span data-ttu-id="bd72c-146">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="bd72c-146">OUTPUTS</span></span>

### <span data-ttu-id="bd72c-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="bd72c-147">System.Object</span></span>

## <span data-ttu-id="bd72c-148">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="bd72c-148">NOTES</span></span>

## <span data-ttu-id="bd72c-149">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="bd72c-149">RELATED LINKS</span></span>

