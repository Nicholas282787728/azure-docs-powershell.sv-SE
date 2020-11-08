---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: d16d9f515544e50cc973b0bb6d5e7fc2455f8a42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917874"
---
# <span data-ttu-id="2c7f6-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="2c7f6-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="2c7f6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2c7f6-102">SYNOPSIS</span></span>
<span data-ttu-id="2c7f6-103">Hämtar ögonblicks bilderna för ett webb program.</span><span class="sxs-lookup"><span data-stu-id="2c7f6-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="2c7f6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2c7f6-104">SYNTAX</span></span>

### <span data-ttu-id="2c7f6-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="2c7f6-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c7f6-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="2c7f6-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-UseDisasterRecovery] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c7f6-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2c7f6-107">DESCRIPTION</span></span>
<span data-ttu-id="2c7f6-108">Cmdleten **Get-AzWebAppSnapshot** returnerar alla stillbilder för ett webb program.</span><span class="sxs-lookup"><span data-stu-id="2c7f6-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="2c7f6-109">Ögonblicks bilder är automatiska säkerhets kopior av filer och inställningar för ett webb program.</span><span class="sxs-lookup"><span data-stu-id="2c7f6-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="2c7f6-110">En ögonblicks bild kan återställas med cmdleten **restore-AzWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="2c7f6-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="2c7f6-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2c7f6-111">EXAMPLES</span></span>

### <span data-ttu-id="2c7f6-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2c7f6-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="2c7f6-113">Hämta stillbilder för ett webb program med namnet "ContosoApp" med en plats med namnet "mellanlagring" i resurs gruppen "default-Web-West"</span><span class="sxs-lookup"><span data-stu-id="2c7f6-113">Get the snapshots for a web app named "ContosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="2c7f6-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2c7f6-114">PARAMETERS</span></span>

### <span data-ttu-id="2c7f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c7f6-115">-DefaultProfile</span></span>
<span data-ttu-id="2c7f6-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2c7f6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c7f6-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="2c7f6-117">-Name</span></span>
<span data-ttu-id="2c7f6-118">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="2c7f6-118">The name of the web app.</span></span>

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

### <span data-ttu-id="2c7f6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c7f6-119">-ResourceGroupName</span></span>
<span data-ttu-id="2c7f6-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2c7f6-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="2c7f6-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="2c7f6-121">-Slot</span></span>
<span data-ttu-id="2c7f6-122">Namnet på Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="2c7f6-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="2c7f6-123">-UseDisasterRecovery</span><span class="sxs-lookup"><span data-stu-id="2c7f6-123">-UseDisasterRecovery</span></span>
<span data-ttu-id="2c7f6-124">Läs stillbilderna från en sekundär skala.</span><span class="sxs-lookup"><span data-stu-id="2c7f6-124">Read the snapshots from a secondary scale unit.</span></span>

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

### <span data-ttu-id="2c7f6-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2c7f6-125">-WebApp</span></span>
<span data-ttu-id="2c7f6-126">Web App-objekt</span><span class="sxs-lookup"><span data-stu-id="2c7f6-126">The web app object</span></span>

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

### <span data-ttu-id="2c7f6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c7f6-127">CommonParameters</span></span>
<span data-ttu-id="2c7f6-128">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c7f6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c7f6-129">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c7f6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c7f6-130">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2c7f6-130">INPUTS</span></span>

### <span data-ttu-id="2c7f6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2c7f6-131">System.String</span></span>

### <span data-ttu-id="2c7f6-132">Microsoft. Azure. commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="2c7f6-132">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2c7f6-133">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2c7f6-133">OUTPUTS</span></span>

### <span data-ttu-id="2c7f6-134">Microsoft. Azure. kommandon. webapps. cmdletar. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="2c7f6-134">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>

## <span data-ttu-id="2c7f6-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2c7f6-135">NOTES</span></span>

## <span data-ttu-id="2c7f6-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2c7f6-136">RELATED LINKS</span></span>