---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B3776B0B-FBC8-407A-A8A4-583C346CCF12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 1c1be584b1110f720d1d5d50b32d7efa5d8586db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757181"
---
# <span data-ttu-id="21b2e-101">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="21b2e-101">Get-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="21b2e-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="21b2e-102">SYNOPSIS</span></span>
<span data-ttu-id="21b2e-103">Hämtar status för en Azure SQL Database Server-uppgradering.</span><span class="sxs-lookup"><span data-stu-id="21b2e-103">Gets the status of an Azure SQL Database server upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21b2e-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="21b2e-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgrade -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21b2e-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="21b2e-105">DESCRIPTION</span></span>
<span data-ttu-id="21b2e-106">Cmdleten **Get-AzureRmSqlServerUpgrade** får statusen för en Azure SQL Database Server-uppgradering.</span><span class="sxs-lookup"><span data-stu-id="21b2e-106">The **Get-AzureRmSqlServerUpgrade** cmdlet gets the status of an Azure SQL Database server upgrade.</span></span>

## <span data-ttu-id="21b2e-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="21b2e-107">EXAMPLES</span></span>

### <span data-ttu-id="21b2e-108">Exempel 1: få en uppgraderings status</span><span class="sxs-lookup"><span data-stu-id="21b2e-108">Example 1: Get the status of an upgrade</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceGroupName               : resourcegroup01
ServerName                      : server01
Status                          : Queued
```

<span data-ttu-id="21b2e-109">Det här kommandot får statusen för en uppgradering från servern med namnet Server01 i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="21b2e-109">This command gets the status of an upgrade from the server named Server01 in resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="21b2e-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="21b2e-110">PARAMETERS</span></span>

### <span data-ttu-id="21b2e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21b2e-111">-DefaultProfile</span></span>
<span data-ttu-id="21b2e-112">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure</span><span class="sxs-lookup"><span data-stu-id="21b2e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21b2e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21b2e-113">-ResourceGroupName</span></span>
<span data-ttu-id="21b2e-114">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="21b2e-114">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21b2e-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="21b2e-115">-ServerName</span></span>
<span data-ttu-id="21b2e-116">Anger namnet på den server där denna cmdlet ska uppgradera.</span><span class="sxs-lookup"><span data-stu-id="21b2e-116">Specifies the name of the server for which this cmdlet gets upgrade status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21b2e-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="21b2e-117">-Confirm</span></span>
<span data-ttu-id="21b2e-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="21b2e-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21b2e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21b2e-119">-WhatIf</span></span>
<span data-ttu-id="21b2e-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="21b2e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21b2e-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="21b2e-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21b2e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21b2e-122">CommonParameters</span></span>
<span data-ttu-id="21b2e-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21b2e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21b2e-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21b2e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21b2e-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="21b2e-125">INPUTS</span></span>

### <span data-ttu-id="21b2e-126">Ingen</span><span class="sxs-lookup"><span data-stu-id="21b2e-126">None</span></span>
<span data-ttu-id="21b2e-127">Denna cmdlet accepterar inte indata.</span><span class="sxs-lookup"><span data-stu-id="21b2e-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="21b2e-128">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="21b2e-128">OUTPUTS</span></span>

### <span data-ttu-id="21b2e-129">Microsoft. Azure. commands. SQL. ServerUpgrade. Model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="21b2e-129">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="21b2e-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="21b2e-130">NOTES</span></span>

## <span data-ttu-id="21b2e-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="21b2e-131">RELATED LINKS</span></span>

[<span data-ttu-id="21b2e-132">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="21b2e-132">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="21b2e-133">Stopp-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="21b2e-133">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="21b2e-134">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="21b2e-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


