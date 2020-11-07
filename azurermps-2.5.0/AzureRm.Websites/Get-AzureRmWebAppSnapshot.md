---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappsnapshot
schema: 2.0.0
ms.openlocfilehash: 754ff798ca001e2c6b5a067f6e6244704fc2f617
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93928953"
---
# <span data-ttu-id="a1745-101">Get-AzureRmWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="a1745-101">Get-AzureRmWebAppSnapshot</span></span>

## <span data-ttu-id="a1745-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="a1745-102">SYNOPSIS</span></span>
<span data-ttu-id="a1745-103">Hämtar ögonblicks bilderna för ett webb program.</span><span class="sxs-lookup"><span data-stu-id="a1745-103">Gets the snapshots available for a web app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1745-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="a1745-104">SYNTAX</span></span>

### <span data-ttu-id="a1745-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="a1745-105">FromResourceName</span></span>
```
Get-AzureRmWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="a1745-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="a1745-106">FromWebApp</span></span>
```
Get-AzureRmWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="a1745-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="a1745-107">DESCRIPTION</span></span>
<span data-ttu-id="a1745-108">Cmdleten **Get-AzureRmWebAppSnapshot** returnerar alla stillbilder för ett webb program.</span><span class="sxs-lookup"><span data-stu-id="a1745-108">The **Get-AzureRmWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="a1745-109">Ögonblicks bilder är automatiska säkerhets kopior av filer och inställningar för ett webb program.</span><span class="sxs-lookup"><span data-stu-id="a1745-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="a1745-110">En ögonblicks bild kan återställas med cmdleten **restore-AzureRmWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="a1745-110">A snapshot can be restored with the **Restore-AzureRmWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="a1745-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="a1745-111">EXAMPLES</span></span>

### <span data-ttu-id="a1745-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="a1745-112">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="a1745-113">Hämta stillbilder för ett webb program med namnet "ConstosoApp" med en plats med namnet "mellanlagring" i resurs gruppen "default-Web-West"</span><span class="sxs-lookup"><span data-stu-id="a1745-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="a1745-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="a1745-114">PARAMETERS</span></span>

### <span data-ttu-id="a1745-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1745-115">-DefaultProfile</span></span>
<span data-ttu-id="a1745-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="a1745-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1745-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="a1745-117">-Name</span></span>
<span data-ttu-id="a1745-118">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="a1745-118">The name of the web app.</span></span>

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

### <span data-ttu-id="a1745-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1745-119">-ResourceGroupName</span></span>
<span data-ttu-id="a1745-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="a1745-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="a1745-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="a1745-121">-Slot</span></span>
<span data-ttu-id="a1745-122">Namnet på Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="a1745-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="a1745-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a1745-123">-WebApp</span></span>
<span data-ttu-id="a1745-124">Web App-objekt</span><span class="sxs-lookup"><span data-stu-id="a1745-124">The web app object</span></span>

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

## <span data-ttu-id="a1745-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="a1745-125">INPUTS</span></span>

### <span data-ttu-id="a1745-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a1745-126">System.String</span></span>
<span data-ttu-id="a1745-127">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="a1745-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>


## <span data-ttu-id="a1745-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="a1745-128">OUTPUTS</span></span>

### <span data-ttu-id="a1745-129">Microsoft. Azure. kommandon. webapps. cmdletar. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="a1745-129">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>


## <span data-ttu-id="a1745-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="a1745-130">NOTES</span></span>

## <span data-ttu-id="a1745-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="a1745-131">RELATED LINKS</span></span>

