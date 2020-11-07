---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSnapshot.md
ms.openlocfilehash: 1374bfb67b3150b2c65841d91fd440a83f791b95
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923349"
---
# <span data-ttu-id="2bc48-101">Get-AzWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="2bc48-101">Get-AzWebAppSnapshot</span></span>

## <span data-ttu-id="2bc48-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2bc48-102">SYNOPSIS</span></span>
<span data-ttu-id="2bc48-103">Hämtar ögonblicks bilderna för ett webb program.</span><span class="sxs-lookup"><span data-stu-id="2bc48-103">Gets the snapshots available for a web app.</span></span>

## <span data-ttu-id="2bc48-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2bc48-104">SYNTAX</span></span>

### <span data-ttu-id="2bc48-105">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="2bc48-105">FromResourceName</span></span>
```
Get-AzWebAppSnapshot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>]
```

### <span data-ttu-id="2bc48-106">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="2bc48-106">FromWebApp</span></span>
```
Get-AzWebAppSnapshot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="2bc48-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2bc48-107">DESCRIPTION</span></span>
<span data-ttu-id="2bc48-108">Cmdleten **Get-AzWebAppSnapshot** returnerar alla stillbilder för ett webb program.</span><span class="sxs-lookup"><span data-stu-id="2bc48-108">The **Get-AzWebAppSnapshot** cmdlet returns all snapshots for a web app.</span></span> <span data-ttu-id="2bc48-109">Ögonblicks bilder är automatiska säkerhets kopior av filer och inställningar för ett webb program.</span><span class="sxs-lookup"><span data-stu-id="2bc48-109">Snapshots are automatic backups of a web app's files and settings.</span></span> <span data-ttu-id="2bc48-110">En ögonblicks bild kan återställas med cmdleten **restore-AzWebAppSnapshot** .</span><span class="sxs-lookup"><span data-stu-id="2bc48-110">A snapshot can be restored with the **Restore-AzWebAppSnapshot** cmdlet.</span></span>

## <span data-ttu-id="2bc48-111">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2bc48-111">EXAMPLES</span></span>

### <span data-ttu-id="2bc48-112">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="2bc48-112">Example 1</span></span>
```
PS C:\> Get-AzWebAppSnapshot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoApp" -Slot "Staging"
```

<span data-ttu-id="2bc48-113">Hämta stillbilder för ett webb program med namnet "ConstosoApp" med en plats med namnet "mellanlagring" i resurs gruppen "default-Web-West"</span><span class="sxs-lookup"><span data-stu-id="2bc48-113">Get the snapshots for a web app named "ConstosoApp" with a slot named "Staging" in the "Default-Web-WestUS" resource group</span></span>

## <span data-ttu-id="2bc48-114">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2bc48-114">PARAMETERS</span></span>

### <span data-ttu-id="2bc48-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bc48-115">-DefaultProfile</span></span>
<span data-ttu-id="2bc48-116">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2bc48-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bc48-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="2bc48-117">-Name</span></span>
<span data-ttu-id="2bc48-118">Namnet på webb programmet.</span><span class="sxs-lookup"><span data-stu-id="2bc48-118">The name of the web app.</span></span>

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

### <span data-ttu-id="2bc48-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bc48-119">-ResourceGroupName</span></span>
<span data-ttu-id="2bc48-120">Namnet på resurs gruppen.</span><span class="sxs-lookup"><span data-stu-id="2bc48-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="2bc48-121">-Plats</span><span class="sxs-lookup"><span data-stu-id="2bc48-121">-Slot</span></span>
<span data-ttu-id="2bc48-122">Namnet på Web App-platsen.</span><span class="sxs-lookup"><span data-stu-id="2bc48-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="2bc48-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2bc48-123">-WebApp</span></span>
<span data-ttu-id="2bc48-124">Web App-objekt</span><span class="sxs-lookup"><span data-stu-id="2bc48-124">The web app object</span></span>

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

## <span data-ttu-id="2bc48-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2bc48-125">INPUTS</span></span>

### <span data-ttu-id="2bc48-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2bc48-126">System.String</span></span>
<span data-ttu-id="2bc48-127">Microsoft. Azure. Management. webbplatser. Models. site</span><span class="sxs-lookup"><span data-stu-id="2bc48-127">Microsoft.Azure.Management.WebSites.Models.Site</span></span>


## <span data-ttu-id="2bc48-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2bc48-128">OUTPUTS</span></span>

### <span data-ttu-id="2bc48-129">Microsoft. Azure. kommandon. webapps. cmdletar. BackupRestore. AzureWebAppSnapshot</span><span class="sxs-lookup"><span data-stu-id="2bc48-129">Microsoft.Azure.Commands.WebApps.Cmdlets.BackupRestore.AzureWebAppSnapshot</span></span>


## <span data-ttu-id="2bc48-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2bc48-130">NOTES</span></span>

## <span data-ttu-id="2bc48-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2bc48-131">RELATED LINKS</span></span>

