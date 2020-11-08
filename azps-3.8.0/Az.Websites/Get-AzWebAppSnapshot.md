---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 350f7d5b44f5a1c84f97511a4febb7d967ee2de4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94089571"
---
# <span data-ttu-id="3e08a-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="3e08a-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="3e08a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="3e08a-102">SYNOPSIS</span></span>
<span data-ttu-id="3e08a-103">Hämtar ögonblicks bilderna för ett webb program.</span><span class="sxs-lookup"><span data-stu-id="3e08a-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="3e08a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="3e08a-104">SYNTAX</span></span>

### <span data-ttu-id="3e08a-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="3e08a-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e08a-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="3e08a-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e08a-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="3e08a-107">DESCRIPTION</span></span>
<span data-ttu-id="3e08a-108">Cmdleten **Get-AzWebAppSnapshot** returnerar alla stillbilder för ett webb program.</span><span class="sxs-lookup"><span data-stu-id="3e08a-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="3e08a-109">Ögonblicks bilder är automatiska säkerhets kopior av filer och inställningar för ett webb program.</span><span class="sxs-lookup"><span data-stu-id="3e08a-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="3e08a-110">En ögonblicks bild kan återställas med cmdleten **restore-AzWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="3e08a-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="3e08a-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="3e08a-111">EXAMPLES</span></span>

### <span data-ttu-id="3e08a-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="3e08a-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="3e08a-113">Hämta stillbilder för ett webb program med namnet "ContosoApp" med en plats med namnet "mellanlagring" i resurs gruppen "default-Web-West"</span><span class="sxs-lookup"><span data-stu-id="3e08a-113">Get the snapshots for a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="3e08a-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="3e08a-114">PARAMETERS</span></span>

### <span data-ttu-id="3e08a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e08a-115">-DefaultProfile</span></span>
<span data-ttu-id="3e08a-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="3e08a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e08a-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="3e08a-117">-Name</span></span>
<span data-ttu-id="3e08a-118">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="3e08a-118">The name of the web app.</span></span>

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

### <span data-ttu-id="3e08a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e08a-119">-ResourceGroupName</span></span>
<span data-ttu-id="3e08a-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="3e08a-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="3e08a-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="3e08a-121">-Slot</span></span>
<span data-ttu-id="3e08a-122">Namnet på Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="3e08a-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="3e08a-123">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="3e08a-123">-UseDisasterRecovery</span></span>
<span data-ttu-id="3e08a-124">Läs stillbilderna från en sekundär skala.</span><span class="sxs-lookup"><span data-stu-id="3e08a-124">Read the snapshots from a secondary scale unit.</span></span>

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

### <span data-ttu-id="3e08a-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3e08a-125">-WebApp</span></span>
<span data-ttu-id="3e08a-126">Web App-objekt</span><span class="sxs-lookup"><span data-stu-id="3e08a-126">The web app object</span></span>

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

### <span data-ttu-id="3e08a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e08a-127">CommonParameters</span></span>
<span data-ttu-id="3e08a-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e08a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e08a-129">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e08a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e08a-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="3e08a-130">INPUTS</span></span>

### <span data-ttu-id="3e08a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3e08a-131">System.String</span></span>

### <span data-ttu-id="3e08a-132">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="3e08a-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="3e08a-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="3e08a-133">OUTPUTS</span></span>

### <span data-ttu-id="3e08a-134">Microsoft. Azure. kommandon. webapps. cmdletar. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="3e08a-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="3e08a-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="3e08a-135">NOTES</span></span>

## <span data-ttu-id="3e08a-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="3e08a-136">RELATED LINKS</span></span>
