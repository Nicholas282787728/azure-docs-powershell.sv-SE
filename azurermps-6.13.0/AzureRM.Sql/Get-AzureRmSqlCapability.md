---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 8C5D29AD-0B15-4CD4-8637-86ABD19F41C8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlcapability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlCapability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlCapability.md
ms.openlocfilehash: e300b5f1fb57f18941d7194aa413a6ef468c626e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757342"
---
# <span data-ttu-id="cc803-101">Get-AzureRmSqlCapability</span><span class="sxs-lookup"><span data-stu-id="cc803-101">Get-AzureRmSqlCapability</span></span>

## <span data-ttu-id="cc803-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="cc803-102">SYNOPSIS</span></span>
<span data-ttu-id="cc803-103">Hämtar SQL-databasens funktioner för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="cc803-103">Gets SQL Database capabilities for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc803-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="cc803-104">SYNTAX</span></span>

### <span data-ttu-id="cc803-105">FilterResults (standard)</span><span class="sxs-lookup"><span data-stu-id="cc803-105">FilterResults (Default)</span></span>
```
Get-AzureRmSqlCapability [-LocationName] <String> [-ServerVersionName <String>] [-EditionName <String>]
 [-ServiceObjectiveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cc803-106">DefaultResults</span><span class="sxs-lookup"><span data-stu-id="cc803-106">DefaultResults</span></span>
```
Get-AzureRmSqlCapability [-LocationName] <String> [-Defaults] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc803-107">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="cc803-107">DESCRIPTION</span></span>
<span data-ttu-id="cc803-108">Cmdleten **Get-AzureRmSqlCapability** hämtar de tillgängliga Azure SQL-databas funktionerna för en region.</span><span class="sxs-lookup"><span data-stu-id="cc803-108">The **Get-AzureRmSqlCapability** cmdlet gets the Azure SQL Database capabilities available on the current subscription for a region.</span></span>
<span data-ttu-id="cc803-109">Om du anger parametrarna *ServerVersionName* , *EditionName* eller *ServiceObjectiveName* returnerar denna cmdlet de angivna värdena och deras föregående aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="cc803-109">If you specify the *ServerVersionName* , *EditionName* , or *ServiceObjectiveName* parameters, this cmdlet returns the specified values and their predecessors.</span></span>

## <span data-ttu-id="cc803-110">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="cc803-110">EXAMPLES</span></span>

### <span data-ttu-id="cc803-111">Exempel 1: få funktioner för det aktuella abonnemanget för en region</span><span class="sxs-lookup"><span data-stu-id="cc803-111">Example 1: Get capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US"
Location                : Central US
Status                  : Available
SupportedServerVersions : {12.0, 2.0}
```

<span data-ttu-id="cc803-112">Det här kommandot returnerar funktionerna för SQL Database-instanser för det aktuella abonnemanget för den centrala amerikanska regionen.</span><span class="sxs-lookup"><span data-stu-id="cc803-112">This command returns the capabilities for SQL Database instances on the current subscription for the Central US region.</span></span>

### <span data-ttu-id="cc803-113">Exempel 2: Hämta standard funktioner för det aktuella abonnemanget för en region</span><span class="sxs-lookup"><span data-stu-id="cc803-113">Example 2: Get default capabilities for the current subscription for a region</span></span>
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US" -Defaults
Location        : Central US
Status          : Available
ExpandedDetails : Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S0 (Default)
```

<span data-ttu-id="cc803-114">Det här kommandot returnerar standard funktionerna för SQL-databaser för det aktuella abonnemanget i den centrala amerikanska regionen.</span><span class="sxs-lookup"><span data-stu-id="cc803-114">This command returns the default capabilities for SQL Databases on the current subscription in the Central US region.</span></span>

### <span data-ttu-id="cc803-115">Exempel 3: få information om ett tjänst mål</span><span class="sxs-lookup"><span data-stu-id="cc803-115">Example 3: Get details for a service objective</span></span>
```
PS C:\>Get-AzureRmSqlCapability -LocationName "Central US" -ServiceObjectiveName "S1"
Location        : Central US
Status          : Available
ExpandedDetails : Version: 12.0 (Available) -> Edition: Standard (Default) -> Service Objective: S1 (Available) 
                  Version: 2.0 (Default) -> Edition: Standard (Default) -> Service Objective: S1 (Available)
```

<span data-ttu-id="cc803-116">Det här kommandot får standard funktioner för SQL-databaser för det angivna tjänst målet för det aktuella abonnemanget.</span><span class="sxs-lookup"><span data-stu-id="cc803-116">This command gets default capabilities for SQL Databases for the specified service objective on the current subscription.</span></span>

## <span data-ttu-id="cc803-117">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="cc803-117">PARAMETERS</span></span>

### <span data-ttu-id="cc803-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc803-118">-DefaultProfile</span></span>
<span data-ttu-id="cc803-119">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="cc803-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc803-120">-Standard</span><span class="sxs-lookup"><span data-stu-id="cc803-120">-Defaults</span></span>
<span data-ttu-id="cc803-121">Anger att denna cmdlet endast får standardvärden.</span><span class="sxs-lookup"><span data-stu-id="cc803-121">Indicates that this cmdlet gets only defaults.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc803-122">-EditionName</span><span class="sxs-lookup"><span data-stu-id="cc803-122">-EditionName</span></span>
<span data-ttu-id="cc803-123">Anger namnet på den databas version som denna cmdlet hämtar funktioner för.</span><span class="sxs-lookup"><span data-stu-id="cc803-123">Specifies the name of the database edition for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc803-124">-LocationName</span><span class="sxs-lookup"><span data-stu-id="cc803-124">-LocationName</span></span>
<span data-ttu-id="cc803-125">Anger namnet på den plats där denna cmdlet får funktioner.</span><span class="sxs-lookup"><span data-stu-id="cc803-125">Specifies the name of the Location for which this cmdlet gets capabilities.</span></span>
<span data-ttu-id="cc803-126">Mer information finns i Azure-regioner https://azure.microsoft.com/en-us/regions/ ( https://azure.microsoft.com/en-us/regions/) .</span><span class="sxs-lookup"><span data-stu-id="cc803-126">For more information, see Azure Regionshttps://azure.microsoft.com/en-us/regions/ (https://azure.microsoft.com/en-us/regions/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc803-127">-ServerVersionName</span><span class="sxs-lookup"><span data-stu-id="cc803-127">-ServerVersionName</span></span>
<span data-ttu-id="cc803-128">Anger namnet på den server version som denna cmdlet hämtar funktioner för.</span><span class="sxs-lookup"><span data-stu-id="cc803-128">Specifies the name of the server version for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc803-129">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="cc803-129">-ServiceObjectiveName</span></span>
<span data-ttu-id="cc803-130">Anger namnet på det tjänst mål som denna cmdlet får funktioner för.</span><span class="sxs-lookup"><span data-stu-id="cc803-130">Specifies the name of the service objective for which this cmdlet gets capabilities.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterResults
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc803-131">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="cc803-131">-Confirm</span></span>
<span data-ttu-id="cc803-132">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="cc803-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc803-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc803-133">-WhatIf</span></span>
<span data-ttu-id="cc803-134">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="cc803-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc803-135">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="cc803-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc803-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc803-136">CommonParameters</span></span>
<span data-ttu-id="cc803-137">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc803-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc803-138">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc803-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc803-139">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="cc803-139">INPUTS</span></span>

### <span data-ttu-id="cc803-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cc803-140">System.String</span></span>

## <span data-ttu-id="cc803-141">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="cc803-141">OUTPUTS</span></span>

### <span data-ttu-id="cc803-142">Microsoft.Azure.Commands.Sql.Location_Capabilities. Model. LocationCapabilityModel</span><span class="sxs-lookup"><span data-stu-id="cc803-142">Microsoft.Azure.Commands.Sql.Location_Capabilities.Model.LocationCapabilityModel</span></span>

## <span data-ttu-id="cc803-143">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="cc803-143">NOTES</span></span>

## <span data-ttu-id="cc803-144">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="cc803-144">RELATED LINKS</span></span>
