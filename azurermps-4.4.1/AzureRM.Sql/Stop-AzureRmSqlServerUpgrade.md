---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 972F4188-52C5-4B92-8B88-E68526537F48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: 1c9940f5278390fc72dbd8e7d906718f01375583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93757437"
---
# <span data-ttu-id="edb84-101">Stop-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="edb84-101">Stop-AzureRmSqlServerUpgrade</span></span>

## <span data-ttu-id="edb84-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="edb84-102">SYNOPSIS</span></span>
<span data-ttu-id="edb84-103">Stoppar uppgraderingen av en SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="edb84-103">Stops the upgrade of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edb84-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="edb84-104">SYNTAX</span></span>

```
Stop-AzureRmSqlServerUpgrade [-Force] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edb84-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="edb84-105">DESCRIPTION</span></span>
<span data-ttu-id="edb84-106">Cmdleten **Stop-AzureRmSqlServerUpgrade** stoppar uppgraderingen av en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="edb84-106">The **Stop-AzureRmSqlServerUpgrade** cmdlet stops the upgrade of an Azure SQL Database server.</span></span>

## <span data-ttu-id="edb84-107">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="edb84-107">EXAMPLES</span></span>

### <span data-ttu-id="edb84-108">Exempel 1: stoppa en Server uppgradering</span><span class="sxs-lookup"><span data-stu-id="edb84-108">Example 1: Stop a server upgrade</span></span>
```
PS C:\>Stop-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server02"
```

<span data-ttu-id="edb84-109">Med det här kommandot stoppas begäran om att uppgradera servern som Server02 tilldelats till resurs gruppen med namnet ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="edb84-109">This command stops the request to upgrade the server named Server02 assigned to the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="edb84-110">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="edb84-110">PARAMETERS</span></span>

### <span data-ttu-id="edb84-111">-Force</span><span class="sxs-lookup"><span data-stu-id="edb84-111">-Force</span></span>
<span data-ttu-id="edb84-112">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="edb84-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="edb84-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edb84-113">-ResourceGroupName</span></span>
<span data-ttu-id="edb84-114">Anger namnet på den resurs grupp som servern är tilldelad till.</span><span class="sxs-lookup"><span data-stu-id="edb84-114">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="edb84-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="edb84-115">-ServerName</span></span>
<span data-ttu-id="edb84-116">Anger namnet på den server där denna cmdlet slutar en uppgradering.</span><span class="sxs-lookup"><span data-stu-id="edb84-116">Specifies the name of the server for which this cmdlet stops an upgrade.</span></span>

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

### <span data-ttu-id="edb84-117">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="edb84-117">-Confirm</span></span>
<span data-ttu-id="edb84-118">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="edb84-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edb84-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edb84-119">-WhatIf</span></span>
<span data-ttu-id="edb84-120">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="edb84-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edb84-121">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="edb84-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edb84-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb84-122">-DefaultProfile</span></span>
<span data-ttu-id="edb84-123">Autentiseringsuppgifter, konto, klient organisation och abonnemang som används för kommunikation med Azure.</span><span class="sxs-lookup"><span data-stu-id="edb84-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edb84-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb84-124">CommonParameters</span></span>
<span data-ttu-id="edb84-125">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edb84-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb84-126">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edb84-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb84-127">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="edb84-127">INPUTS</span></span>

### <span data-ttu-id="edb84-128">Microsoft. Azure. commands. SQL. ServerUpgrade. Model. AzureSqlServerUpgradeModel</span><span class="sxs-lookup"><span data-stu-id="edb84-128">Microsoft.Azure.Commands.Sql.ServerUpgrade.Model.AzureSqlServerUpgradeModel</span></span>

## <span data-ttu-id="edb84-129">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="edb84-129">OUTPUTS</span></span>

## <span data-ttu-id="edb84-130">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="edb84-130">NOTES</span></span>

## <span data-ttu-id="edb84-131">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="edb84-131">RELATED LINKS</span></span>

[<span data-ttu-id="edb84-132">Get-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="edb84-132">Get-AzureRmSqlServerUpgrade</span></span>](./Get-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="edb84-133">Start-AzureRmSqlServerUpgrade</span><span class="sxs-lookup"><span data-stu-id="edb84-133">Start-AzureRmSqlServerUpgrade</span></span>](./Start-AzureRmSqlServerUpgrade.md)

[<span data-ttu-id="edb84-134">Dokumentation för SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="edb84-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


