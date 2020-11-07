---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 0FDDDEE1-CEAD-46DA-A7EB-EE477ED59749
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/start-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Start-AzWebAppSlot.md
ms.openlocfilehash: d843cf5eed70e230f81c704e9168fee917a77077
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93923253"
---
# <span data-ttu-id="19677-101">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="19677-101">Start-AzWebAppSlot</span></span>

## <span data-ttu-id="19677-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="19677-102">SYNOPSIS</span></span>
<span data-ttu-id="19677-103">Startar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="19677-103">Starts an Azure Web App slot.</span></span>

## <span data-ttu-id="19677-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="19677-104">SYNTAX</span></span>

### <span data-ttu-id="19677-105">S</span><span class="sxs-lookup"><span data-stu-id="19677-105">S1</span></span>
```
Start-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19677-106">S2</span><span class="sxs-lookup"><span data-stu-id="19677-106">S2</span></span>
```
Start-AzWebAppSlot [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19677-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="19677-107">DESCRIPTION</span></span>
<span data-ttu-id="19677-108">Cmdleten **Start-AzWebAppSlot** startar en Azure Web App-plats.</span><span class="sxs-lookup"><span data-stu-id="19677-108">The **Start-AzWebAppSlot** cmdlet starts an Azure Web App Slot.</span></span>

## <span data-ttu-id="19677-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="19677-109">EXAMPLES</span></span>

### <span data-ttu-id="19677-110">Exempel 1</span><span class="sxs-lookup"><span data-stu-id="19677-110">Example 1</span></span>
```
PS C:\>Start-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001"
```

<span data-ttu-id="19677-111">Det här kommandot startar facket som heter Slot001 som hör till webb programmet som heter ContosoWebApp och som tillhör resurs gruppen som heter default-West-väst.</span><span class="sxs-lookup"><span data-stu-id="19677-111">This command starts the Slot named Slot001 pertaining to the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="19677-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="19677-112">PARAMETERS</span></span>

### <span data-ttu-id="19677-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19677-113">-DefaultProfile</span></span>
<span data-ttu-id="19677-114">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="19677-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19677-115">-Namn</span><span class="sxs-lookup"><span data-stu-id="19677-115">-Name</span></span>
<span data-ttu-id="19677-116">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="19677-116">WebApp Name</span></span>

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

### <span data-ttu-id="19677-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19677-117">-ResourceGroupName</span></span>
<span data-ttu-id="19677-118">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="19677-118">Resource Group Name</span></span>

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

### <span data-ttu-id="19677-119">-Plats</span><span class="sxs-lookup"><span data-stu-id="19677-119">-Slot</span></span>
<span data-ttu-id="19677-120">WebApp-slot</span><span class="sxs-lookup"><span data-stu-id="19677-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="19677-121">-WebApp</span><span class="sxs-lookup"><span data-stu-id="19677-121">-WebApp</span></span>
<span data-ttu-id="19677-122">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="19677-122">WebApp Object</span></span>

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

### <span data-ttu-id="19677-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19677-123">CommonParameters</span></span>
<span data-ttu-id="19677-124">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19677-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19677-125">Mer information finns i about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19677-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19677-126">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="19677-126">INPUTS</span></span>

### <span data-ttu-id="19677-127">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="19677-127">Site</span></span>
<span data-ttu-id="19677-128">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="19677-128">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="19677-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="19677-129">OUTPUTS</span></span>

## <span data-ttu-id="19677-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="19677-130">NOTES</span></span>

## <span data-ttu-id="19677-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="19677-131">RELATED LINKS</span></span>

[<span data-ttu-id="19677-132">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="19677-132">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="19677-133">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="19677-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="19677-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="19677-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="19677-135">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="19677-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="19677-136">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="19677-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="19677-137">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="19677-137">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="19677-138">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="19677-138">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
