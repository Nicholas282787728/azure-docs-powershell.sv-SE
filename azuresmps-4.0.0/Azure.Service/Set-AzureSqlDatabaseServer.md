---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B5A2F2A8-5D20-47E4-AFC5-44F687142A08
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e40d833125725f0ae1baff920a283112db24cdc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94099094"
---
# <span data-ttu-id="c88d6-101">Set-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="c88d6-101">Set-AzureSqlDatabaseServer</span></span>

## <span data-ttu-id="c88d6-102">Sammanfattning</span><span class="sxs-lookup"><span data-stu-id="c88d6-102">SYNOPSIS</span></span>
<span data-ttu-id="c88d6-103">Ändrar egenskaper för en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="c88d6-103">Modifies the properties of an Azure SQL Database server.</span></span>

## <span data-ttu-id="c88d6-104">FRÅGESYNTAXEN</span><span class="sxs-lookup"><span data-stu-id="c88d6-104">SYNTAX</span></span>

```
Set-AzureSqlDatabaseServer -ServerName <String> -AdminPassword <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c88d6-105">PROBLEMBESKRIVNING</span><span class="sxs-lookup"><span data-stu-id="c88d6-105">DESCRIPTION</span></span>
<span data-ttu-id="c88d6-106">Cmdleten **set-AzureSqlDatabaseServer** ändrar egenskaperna för den angivna instansen av en Azure SQL Database-Server.</span><span class="sxs-lookup"><span data-stu-id="c88d6-106">The **Set-AzureSqlDatabaseServer** cmdlet modifies the properties of the specified instance of Azure SQL Database Server.</span></span>
<span data-ttu-id="c88d6-107">I den aktuella versionen kan du bara uppdatera lösen ordet för administratörs kontot för en server.</span><span class="sxs-lookup"><span data-stu-id="c88d6-107">In the current release, you can only update the administrator account password for a server.</span></span>

## <span data-ttu-id="c88d6-108">BESKRIVS</span><span class="sxs-lookup"><span data-stu-id="c88d6-108">EXAMPLES</span></span>

### <span data-ttu-id="c88d6-109">Exempel 1: ändra lösen ordet för en server</span><span class="sxs-lookup"><span data-stu-id="c88d6-109">Example 1: Change the password for a server</span></span>
```
PS C:\>Set-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y" -AdminPassword "NewPassword"
```

<span data-ttu-id="c88d6-110">Det här kommandot ändrar lösen ordet för din Azure SQL-databas med namnet lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="c88d6-110">This command changes the administrator account password for the Azure SQL Database server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="c88d6-111">MALLPARAMETRAR</span><span class="sxs-lookup"><span data-stu-id="c88d6-111">PARAMETERS</span></span>

### <span data-ttu-id="c88d6-112">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="c88d6-112">-AdminPassword</span></span>
<span data-ttu-id="c88d6-113">Anger lösen ordet för administratörs kontot för Azure SQL Database-servern.</span><span class="sxs-lookup"><span data-stu-id="c88d6-113">Specifies the administrator account password for the Azure SQL Database server.</span></span>
<span data-ttu-id="c88d6-114">Du måste ange ett starkt lösen ord.</span><span class="sxs-lookup"><span data-stu-id="c88d6-114">You must specify a strong password.</span></span>
<span data-ttu-id="c88d6-115">Mer information finns i [starka lösen ord](https://go.microsoft.com/fwlink/p/?LinkId=154152) ( https://go.microsoft.com/fwlink/p/?LinkId=154152) på Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="c88d6-115">For more information, see [Strong Passwords](https://go.microsoft.com/fwlink/p/?LinkId=154152) (https://go.microsoft.com/fwlink/p/?LinkId=154152) at the Microsoft Developer Network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88d6-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c88d6-116">-Force</span></span>
<span data-ttu-id="c88d6-117">Tvingar kommandot att köras utan att fråga efter bekräftelse.</span><span class="sxs-lookup"><span data-stu-id="c88d6-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88d6-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="c88d6-118">-Profile</span></span>
<span data-ttu-id="c88d6-119">Anger den Azure-profil från vilken denna cmdlet läser.</span><span class="sxs-lookup"><span data-stu-id="c88d6-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c88d6-120">Om du inte anger en profil läser denna cmdlet från den lokala standard profilen.</span><span class="sxs-lookup"><span data-stu-id="c88d6-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c88d6-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c88d6-121">-ServerName</span></span>
<span data-ttu-id="c88d6-122">Anger namnet på den server som cmdleten ändrar.</span><span class="sxs-lookup"><span data-stu-id="c88d6-122">Specifies the name of the server that this cmdlet modifies.</span></span>
<span data-ttu-id="c88d6-123">Ange Server namnet, inte det fullständigt kvalificerade DNS-namnet.</span><span class="sxs-lookup"><span data-stu-id="c88d6-123">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="c88d6-124">-Bekräfta</span><span class="sxs-lookup"><span data-stu-id="c88d6-124">-Confirm</span></span>
<span data-ttu-id="c88d6-125">Du uppmanas att bekräfta innan du kör cmdleten.</span><span class="sxs-lookup"><span data-stu-id="c88d6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c88d6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c88d6-126">-WhatIf</span></span>
<span data-ttu-id="c88d6-127">Visar vad som händer om cmdleten körs.</span><span class="sxs-lookup"><span data-stu-id="c88d6-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c88d6-128">Cmdleten körs inte.</span><span class="sxs-lookup"><span data-stu-id="c88d6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c88d6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c88d6-129">CommonParameters</span></span>
<span data-ttu-id="c88d6-130">Den här cmdleten har stöd för de gemensamma parametrarna:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-disvariable,-utbuffer,-PipelineVariable,-verbose,-WarningAction och-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c88d6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c88d6-131">Mer information finns i about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c88d6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c88d6-132">KOSTNADS</span><span class="sxs-lookup"><span data-stu-id="c88d6-132">INPUTS</span></span>

### <span data-ttu-id="c88d6-133">Microsoft. WindowsAzure. kommandon. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="c88d6-133">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

## <span data-ttu-id="c88d6-134">VÄRDEN</span><span class="sxs-lookup"><span data-stu-id="c88d6-134">OUTPUTS</span></span>

## <span data-ttu-id="c88d6-135">ANMÄRKNINGAR</span><span class="sxs-lookup"><span data-stu-id="c88d6-135">NOTES</span></span>

## <span data-ttu-id="c88d6-136">RELATERADE LÄNKAR</span><span class="sxs-lookup"><span data-stu-id="c88d6-136">RELATED LINKS</span></span>

[<span data-ttu-id="c88d6-137">Azure SQL-databas</span><span class="sxs-lookup"><span data-stu-id="c88d6-137">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="c88d6-138">Åtgärder för Azure SQL-databaser</span><span class="sxs-lookup"><span data-stu-id="c88d6-138">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="c88d6-139">Get-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="c88d6-139">Get-AzureSqlDatabaseServer</span></span>](./Get-AzureSqlDatabaseServer.md)

[<span data-ttu-id="c88d6-140">New-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="c88d6-140">New-AzureSqlDatabaseServer</span></span>](./New-AzureSqlDatabaseServer.md)

[<span data-ttu-id="c88d6-141">Remove-AzureSqlDatabaseServer</span><span class="sxs-lookup"><span data-stu-id="c88d6-141">Remove-AzureSqlDatabaseServer</span></span>](./Remove-AzureSqlDatabaseServer.md)


