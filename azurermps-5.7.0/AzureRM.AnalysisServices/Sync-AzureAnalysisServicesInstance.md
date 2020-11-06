---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: f3fb2377fd78db4b330afd39a8691f958597f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574957"
---
# <span data-ttu-id="cdf7a-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="cdf7a-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="cdf7a-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cdf7a-102">SYNOPSIS</span></span>

<span data-ttu-id="cdf7a-103">Synkroniserar en angiven databas på den angivna instansen av Analysis Services-servern till alla instanser av den aktuella inloggade miljön enligt vad som anges i Add-AzureAnalysisServicesAccount kommando</span><span class="sxs-lookup"><span data-stu-id="cdf7a-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdf7a-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cdf7a-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-Passthru]
```

## <span data-ttu-id="cdf7a-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cdf7a-105">DESCRIPTION</span></span>

<span data-ttu-id="cdf7a-106">Sync-AzureAnalysisServicesInstance-cmdleten synkroniserar en angiven databas på den angivna instansen av Analysis Services-servern till alla förekomster av den aktuella inloggade miljön enligt vad som anges i Add-AzureAnalysisServicesAccount kommando</span><span class="sxs-lookup"><span data-stu-id="cdf7a-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="cdf7a-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cdf7a-107">EXAMPLES</span></span>

### <span data-ttu-id="cdf7a-108">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="cdf7a-108">Example 1</span></span>

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="cdf7a-109">Det här kommandot synkroniserar databasen med namnet SalesOrders i servern med namnet "contoso" i miljön westus.asazure.windows.net förutsatt att användaren har loggat in på den här enviroment med kommandot Add-AzureAnalysisServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="cdf7a-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="cdf7a-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cdf7a-110">PARAMETERS</span></span>

### <span data-ttu-id="cdf7a-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="cdf7a-111">-Instance</span></span>

<span data-ttu-id="cdf7a-112">Namn på Analysis Services-serverinstansen som ska startas om</span><span class="sxs-lookup"><span data-stu-id="cdf7a-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdf7a-113">-Databas</span><span class="sxs-lookup"><span data-stu-id="cdf7a-113">-Database</span></span>

<span data-ttu-id="cdf7a-114">Identitet för databasen som ska synkroniseras</span><span class="sxs-lookup"><span data-stu-id="cdf7a-114">Identity of the database to be synchronized</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdf7a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdf7a-115">-PassThru</span></span>

<span data-ttu-id="cdf7a-116">Om du anger detta returneras sant om kommandot lyckades.</span><span class="sxs-lookup"><span data-stu-id="cdf7a-116">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: Switch
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="cdf7a-117">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cdf7a-117">INPUTS</span></span>

### <span data-ttu-id="cdf7a-118">Ingen</span><span class="sxs-lookup"><span data-stu-id="cdf7a-118">None</span></span>
<span data-ttu-id="cdf7a-119">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="cdf7a-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cdf7a-120">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cdf7a-120">OUTPUTS</span></span>

### <span data-ttu-id="cdf7a-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cdf7a-121">System.Boolean</span></span>

## <span data-ttu-id="cdf7a-122">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cdf7a-122">NOTES</span></span>

<span data-ttu-id="cdf7a-123">Alias: Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="cdf7a-123">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="cdf7a-124">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cdf7a-124">RELATED LINKS</span></span>
