---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 86E0D477-DD32-49BD-82E7-1CF191E4F612
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/stop-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Stop-AzWebAppSlot.md
ms.openlocfilehash: 4ac4482cb5972553b1dad3972200d2f0eb032fe4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923226"
---
# <span data-ttu-id="99b5b-101">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="99b5b-101">Stop-AzWebAppSlot</span></span>

## <span data-ttu-id="99b5b-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="99b5b-102">SYNOPSIS</span></span>
<span data-ttu-id="99b5b-103">Stoppar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="99b5b-103">Stops an Azure Web App slot.</span></span>

## <span data-ttu-id="99b5b-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="99b5b-104">SYNTAX</span></span>

### <span data-ttu-id="99b5b-105">S</span><span class="sxs-lookup"><span data-stu-id="99b5b-105">S1</span></span>
```
Stop-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99b5b-106">S2</span><span class="sxs-lookup"><span data-stu-id="99b5b-106">S2</span></span>
```
Stop-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99b5b-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="99b5b-107">DESCRIPTION</span></span>
<span data-ttu-id="99b5b-108">Cmdleten **Stop-AzWebAppSlot** stoppar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="99b5b-108">The **Stop-AzWebAppSlot** cmdlet stops an Azure Web App Slot.</span></span>

## <span data-ttu-id="99b5b-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="99b5b-109">EXAMPLES</span></span>

### <span data-ttu-id="99b5b-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="99b5b-110">Example 1</span></span>
```
PS C:\>Stop-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="99b5b-111">Det här kommandot stoppar fack Slot001 för webb programmet som heter ContosoWebApp som tillhör resurs gruppen med namnet default-Web-West.</span><span class="sxs-lookup"><span data-stu-id="99b5b-111">This command stops the slot Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="99b5b-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="99b5b-112">PARAMETERS</span></span>

### <span data-ttu-id="99b5b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99b5b-113">-DefaultProfile</span></span>
<span data-ttu-id="99b5b-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="99b5b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99b5b-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="99b5b-115">-Name</span></span>
<span data-ttu-id="99b5b-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="99b5b-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99b5b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99b5b-117">-ResourceGroupName</span></span>
<span data-ttu-id="99b5b-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="99b5b-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b5b-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="99b5b-119">-Slot</span></span>
<span data-ttu-id="99b5b-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="99b5b-120">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99b5b-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="99b5b-121">-WebApp</span></span>
<span data-ttu-id="99b5b-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="99b5b-122">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99b5b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99b5b-123">CommonParameters</span></span>
<span data-ttu-id="99b5b-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99b5b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99b5b-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99b5b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99b5b-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="99b5b-126">INPUTS</span></span>

### <span data-ttu-id="99b5b-127">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="99b5b-127">Site</span></span>
<span data-ttu-id="99b5b-128">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="99b5b-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="99b5b-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="99b5b-129">OUTPUTS</span></span>

## <span data-ttu-id="99b5b-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="99b5b-130">NOTES</span></span>

## <span data-ttu-id="99b5b-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="99b5b-131">RELATED LINKS</span></span>

