---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B3776B0B-FBC8-407A-A8A4-583C346CCF12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: d2a92e7209745873364b5de114916bc48b0a3b42
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93574502"
---
# <span data-ttu-id="e578d-101">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="e578d-101">Get-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="e578d-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="e578d-102">SYNOPSIS</span></span>
<span data-ttu-id="e578d-103">Hämtar status för en Azure SQL Database Server-uppgradering.</span><span class="sxs-lookup"><span data-stu-id="e578d-103">Gets the status of an Azure SQL Database server upgrade.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e578d-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="e578d-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgrade -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e578d-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="e578d-105">DESCRIPTION</span></span>
<span data-ttu-id="e578d-106">Cmdleten **Get-AzureRmSqlServerUpgrade** får statusen för en Azure SQL Database Server-uppgradering.</span><span class="sxs-lookup"><span data-stu-id="e578d-106">The **Get-AzureRmSqlServerUpgrade** cmdlet gets the status of an Azure SQL Database server upgrade.</span></span>

## <span data-ttu-id="e578d-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="e578d-107">EXAMPLES</span></span>

### <span data-ttu-id="e578d-108">Exempel 1: få en uppgraderings status</span><span class="sxs-lookup"><span data-stu-id="e578d-108">Example 1: Get the status of an upgrade</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Format-List
ResourceGroupName               : resourcegroup01
ServerName                      : server01
Status                          : Queued
```

<span data-ttu-id="e578d-109">Det här kommandot får statusen för en uppgradering från servern med namnet Server01 i resurs gruppen "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e578d-109">This command gets the status of an upgrade from the server named Server01 in resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="e578d-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="e578d-110">PARAMETERS</span></span>

### <span data-ttu-id="e578d-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e578d-111">-ResourceGroupName</span></span>
<span data-ttu-id="e578d-112">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="e578d-112">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e578d-113">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e578d-113">-ServerName</span></span>
<span data-ttu-id="e578d-114">Anger namnet på den server där denna cmdlet ska uppgradera.</span><span class="sxs-lookup"><span data-stu-id="e578d-114">Specifies the name of the server for which this cmdlet gets upgrade status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e578d-115">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="e578d-115">-Confirm</span></span>
<span data-ttu-id="e578d-116">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="e578d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e578d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e578d-117">-WhatIf</span></span>
<span data-ttu-id="e578d-118">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="e578d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e578d-119">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="e578d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e578d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e578d-120">-DefaultProfile</span></span>
<span data-ttu-id="e578d-121">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="e578d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e578d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e578d-122">CommonParameters</span></span>
<span data-ttu-id="e578d-123">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e578d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e578d-124">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e578d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e578d-125">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="e578d-125">INPUTS</span></span>

## <span data-ttu-id="e578d-126">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="e578d-126">OUTPUTS</span></span>

### <span data-ttu-id="e578d-127">Microsoft. Azure. commands. SQL. ServerUpgrade. Model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="e578d-127">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="e578d-128">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="e578d-128">NOTES</span></span>

## <span data-ttu-id="e578d-129">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="e578d-129">RELATED LINKS</span></span>

[<span data-ttu-id="e578d-130">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="e578d-130">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="e578d-131">Stopp-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="e578d-131">Stop-AzureRmSqlServerUpgrade</span></span>](./Stop-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="e578d-132">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="e578d-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


