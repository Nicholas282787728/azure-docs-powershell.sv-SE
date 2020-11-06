---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 7DBF937E-2D01-4356-9A5F-C5A4CB6D1A10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlotConfigName.md
ms.openlocfilehash: 3ed7bd25c394c2bef5cb3636a4f8c238f45a3558
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573600"
---
# <span data-ttu-id="2379d-101">Set-AzureRmWebAppSlotConfigName</span><span class="sxs-lookup"><span data-stu-id="2379d-101">Set-AzureRmWebAppSlotConfigName</span></span>

## <span data-ttu-id="2379d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="2379d-102">SYNOPSIS</span></span>
<span data-ttu-id="2379d-103">Ange webb program plats konfigurations namn</span><span class="sxs-lookup"><span data-stu-id="2379d-103">Set Web App Slot Config names</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2379d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="2379d-104">SYNTAX</span></span>

### <span data-ttu-id="2379d-105">S</span><span class="sxs-lookup"><span data-stu-id="2379d-105">S1</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2379d-106">S2</span><span class="sxs-lookup"><span data-stu-id="2379d-106">S2</span></span>
```
Set-AzureRmWebAppSlotConfigName [[-AppSettingNames] <String[]>] [[-ConnectionStringNames] <String[]>]
 [-RemoveAllAppSettingNames] [-RemoveAllConnectionStringNames] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2379d-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="2379d-107">DESCRIPTION</span></span>
<span data-ttu-id="2379d-108">Cmdleten **set-AzureRmWebAppSlotConfigName** anger program inställningar och anslutnings strängar som plats inställningar</span><span class="sxs-lookup"><span data-stu-id="2379d-108">The **Set-AzureRmWebAppSlotConfigName** cmdlet marks App Settings and Connection Strings as slot settings</span></span>

## <span data-ttu-id="2379d-109">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="2379d-109">EXAMPLES</span></span>

### <span data-ttu-id="2379d-110">9.1</span><span class="sxs-lookup"><span data-stu-id="2379d-110">1:</span></span>
```
PS C:\> Set-AzureRmWebAppSlotConfigName -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -RemoveAllAppSettingNames -RemoveAllConnectionStringNames
```

<span data-ttu-id="2379d-111">Det här kommandot tar bort alla program inställningar och anslutnings strängar för webb programmet ContosoWebApp som är kopplade till resurs gruppens standard-väst</span><span class="sxs-lookup"><span data-stu-id="2379d-111">This command removes all app settings and connection strings for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="2379d-112">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="2379d-112">PARAMETERS</span></span>

### <span data-ttu-id="2379d-113">-AppSettingNames</span><span class="sxs-lookup"><span data-stu-id="2379d-113">-AppSettingNames</span></span>
<span data-ttu-id="2379d-114">Program inställningar namn sträng mat ris</span><span class="sxs-lookup"><span data-stu-id="2379d-114">App Settings Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2379d-115">-ConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="2379d-115">-ConnectionStringNames</span></span>
<span data-ttu-id="2379d-116">Sträng mat ris namn</span><span class="sxs-lookup"><span data-stu-id="2379d-116">Connection String Names String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2379d-117">-Namn</span><span class="sxs-lookup"><span data-stu-id="2379d-117">-Name</span></span>
<span data-ttu-id="2379d-118">WebApp-namn</span><span class="sxs-lookup"><span data-stu-id="2379d-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2379d-119">-RemoveAllAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="2379d-119">-RemoveAllAppSettingNames</span></span>
<span data-ttu-id="2379d-120">Alternativet ta bort alla namn för program inställningar</span><span class="sxs-lookup"><span data-stu-id="2379d-120">Remove All App Setting Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2379d-121">-RemoveAllConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="2379d-121">-RemoveAllConnectionStringNames</span></span>
<span data-ttu-id="2379d-122">Ta bort alla namn alternativ för anslutnings strängar</span><span class="sxs-lookup"><span data-stu-id="2379d-122">Remove All Connection String Names Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2379d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2379d-123">-ResourceGroupName</span></span>
<span data-ttu-id="2379d-124">Resurs grupps namn</span><span class="sxs-lookup"><span data-stu-id="2379d-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2379d-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2379d-125">-WebApp</span></span>
<span data-ttu-id="2379d-126">WebApp-objekt</span><span class="sxs-lookup"><span data-stu-id="2379d-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2379d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2379d-127">-DefaultProfile</span></span>
<span data-ttu-id="2379d-128">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="2379d-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2379d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2379d-129">CommonParameters</span></span>
<span data-ttu-id="2379d-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2379d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2379d-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2379d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2379d-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="2379d-132">INPUTS</span></span>

### <span data-ttu-id="2379d-133">Webbplatsmallar</span><span class="sxs-lookup"><span data-stu-id="2379d-133">Site</span></span>
<span data-ttu-id="2379d-134">Parametern ' WebApp ' godkänner värdet av typen ' site ' från pipeline</span><span class="sxs-lookup"><span data-stu-id="2379d-134">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="2379d-135">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="2379d-135">OUTPUTS</span></span>

## <span data-ttu-id="2379d-136">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="2379d-136">NOTES</span></span>

## <span data-ttu-id="2379d-137">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="2379d-137">RELATED LINKS</span></span>

